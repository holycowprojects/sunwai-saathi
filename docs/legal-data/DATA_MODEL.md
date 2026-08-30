# Legal-data model and lifecycle

**Status:** Initial technical design; not legal/RTI approval

**Schema generation:** 1

**Last reviewed:** 30 August 2026

This document defines the contracts shared by legal research, deterministic drafting and future source-health tooling. A schema-valid record is not automatically legally correct or filing-ready.

## Record contracts

| Record | Schema | Purpose |
|---|---|---|
| Primary source | `data/schemas/source.schema.json` | Provenance, checksum and independent review decisions |
| Jurisdiction | `data/schemas/jurisdiction.schema.json` | Aggregated application and first-appeal behavior |
| Legal rule | `data/schemas/legal-rule.schema.json` | One effective-dated deterministic legal or portal rule |
| Authority | `data/schemas/authority.schema.json` | PIO and FAA offices identified by designation, never a person's name |
| Source-health report | `data/schemas/source-health-report.schema.json` | Immutable output from a periodic URL/checksum check |

## Lifecycle semantics

| State | Meaning | Filing-ready export |
|---|---|---|
| `research` | Evidence is incomplete or a required review is pending | Blocked |
| `technical-reviewed` | Provenance and transcription passed technical review | Blocked |
| `filing-ready` | Technical and legal/RTI reviews are approved, required dates exist, and the record is not stale | Allowed only when all dependent records are also filing-ready |
| `stale` | The review-by date has passed or a dependency changed | Blocked until reviewed |
| `unsupported` | The product cannot safely represent this behavior | Blocked with a plain-language explanation |
| `disabled` | Withdrawn from active use without deleting history | Blocked |

`filing-ready` is conjunctive: jurisdiction, every consumed legal rule, the selected authority, and every controlling source must pass their own gates. Schema validation is necessary but insufficient. At runtime, a date on or after `staleAfter` blocks a new filing-ready export. A checksum change blocks affected records until reviewed; it never updates an approved value automatically.

## Review rules

- Technical review confirms official provenance, transcription, scope, dates, checksum metadata and internal consistency.
- Legal/RTI review confirms applicability and wording. It cannot be inferred from technical review.
- Language review is additionally required for protected Hindi content.
- Reviewer fields contain a role or stable public reviewer identifier, not private contact details.
- Authority records contain office designations and service addresses only. Personal officer names, phone numbers and personal email addresses are prohibited.

## Version formats

- Application releases use Semantic Versioning: `MAJOR.MINOR.PATCH`; Git tags add `v`, for example `v1.2.0`.
- The legal dataset uses `YYYY.MM.REVISION`, for example `2026.08.6`. `REVISION` increments for every published dataset change in that month and never resets within the month.
- Schema contracts use independent Semantic Versioning. A breaking field or semantic change increments the schema major version.
- A submission pack records the exact application version, legal-data version, jurisdiction profile version and authority record ID.

Legal-data versions describe the dataset build, not the law's effective date. Individual rules retain `effectiveFrom` and optional `effectiveTo` dates.

## Cross-record invariants

1. Every `sourceId` resolves to exactly one source record.
2. IDs are unique within and across their record type.
3. Jurisdiction-specific references cannot silently resolve to a different jurisdiction; national sources may be shared.
4. An effective end date cannot precede its start date.
5. `staleAfter` must follow `reviewedAt` when both exist.
6. A filing-ready jurisdiction cannot depend on a disputed, unsupported, superseded or unapproved source.
7. Central and Delhi profiles remain distinct even when a rule or source is shared.
8. Authority PIO and FAA data must include designation and complete service address; absence produces a non-filing-ready pack.
9. No checksum or URL-health result changes legal behavior without review.

## Monthly source-health output

Each run creates an untracked or CI-artifact JSON report conforming to `source-health-report.schema.json`. It records URL health and checksum observations separately because a reachable URL does not prove unchanged content and unchanged bytes do not prove continuing legal effect.

A record sets `reviewRequired` when a URL breaks, redirects unexpectedly, changes checksum, has no checksum baseline where one is required, or approaches its freshness boundary. Reports never contain downloaded source bytes, credentials, applicant information or case text. Source downloads remain outside Git and are never executed.

## Validation evidence

The initial design was checked against all five jurisdiction dossiers and current structured profiles on 30 August 2026:

- all five profiles use independent IDs and date-oriented legal-data versions;
- all source references resolve to the structured source inventory;
- nullable values preserve documented unknowns rather than inventing defaults;
- research status correctly blocks each currently unapproved profile; and
- the authority schema can represent online, postal and in-person routes without storing personal officer names.

The repository still needs an executable standards-compliant JSON Schema validator during the Milestone 2 stack spike. Until then, structural JSON parsing and cross-reference checks are technical consistency evidence, not full schema-validation evidence.
