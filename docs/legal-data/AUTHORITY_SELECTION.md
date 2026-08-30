# Authority selection methodology

**Status:** Technical research methodology; no authority selected yet

**Last reviewed:** 30 August 2026

SunwaiSaathi will support 5–10 public authorities per jurisdiction in the MVP. Selection must balance genuine citizen usefulness with the ability to maintain correct PIO, FAA, address and filing-route data. A high score never makes an authority filing-ready by itself.

## Evidence order

1. Use current official RTI or grievance statistics that identify public authorities and define the reporting period and measure.
2. Prefer multi-period official data when categories are comparable; record breaks in methodology.
3. When adequate official ranking statistics do not exist, use the fallback rubric below and label the record `fallback-rubric`.
4. Never substitute search popularity, news coverage, anecdote, competitor lists or model-generated rankings for official evidence.
5. Secondary material may help discover an official source but cannot determine a score or filing behavior.

Statistics from different jurisdictions are not directly compared. Their purpose is to rank candidates within the same jurisdiction, not to claim relative government performance.

## Hard verification gates

A candidate cannot become a verified launch candidate unless all gates are true:

- the public authority's identity and jurisdiction are supported by a current official source;
- a PIO office/designation is supported by an official source;
- an FAA office/designation is supported by an official source;
- a complete service address is supported by an official source;
- at least one current filing route is supported by an official source; and
- the evidence is inside its review window and has no unresolved conflict.

Records use office designations, never the name of the person currently holding the post. A portal dropdown alone can prove online coverage but cannot prove a postal PIO/FAA address. Missing or stale FAA data blocks filing-ready first-appeal addressing even when RTI application routing is otherwise supported.

## Fallback rubric

Each dimension receives an integer score from 0 to 4 with a source-backed rationale. The weighted total is:

`total = populationServed/4*20 + grievanceRelevance/4*30 + sourceCompleteness/4*25 + filingAccessibility/4*15 + maintainability/4*10`

| Dimension | Weight | 0 | 1 | 2 | 3 | 4 |
|---|---:|---|---|---|---|---|
| Population served | 20 | No defensible reach evidence | Narrow specialist/local reach | Material but limited population | Broad jurisdiction reach | Near-universal jurisdiction reach |
| Grievance relevance | 30 | Outside stuck-grievance scope | Rare/indirect grievance connection | Recurring but bounded connection | Common citizen-service grievance connection | Core high-volume grievance domain in official evidence |
| Source completeness | 25 | Authority identity unclear | Identity only | Identity plus partial PIO/FAA/route data | Most required directory evidence, with explicit gaps | Current official identity, PIO, FAA, address and route evidence |
| Filing accessibility | 15 | No usable verified route | Route is unclear or impractical | One verified offline route | Verified online route or multiple usable offline routes | Verified online and maintainable offline routes with clear guidance |
| Maintainability | 10 | Volatile, person-named or unversioned evidence | Fragmented pages with no stable directory | Official evidence exists but needs frequent manual reconstruction | Stable official directory with reviewable updates | Stable, date/version-marked official directory and predictable update path |

### Scoring safeguards

- Use `0` when evidence is absent; do not award a neutral midpoint for unknowns.
- Every dimension records its own source IDs and rationale.
- `sourceCompleteness` below 3 prevents selection, regardless of total.
- `maintainability` below 2 prevents selection, regardless of total.
- A total below 60 cannot be shortlisted.
- Scores from 60 to below 75 may be shortlisted for further evidence.
- Scores of 75 or more may become `selected-pending-verification`; all hard gates must still pass before `verified-launch-candidate`.
- A disputed source, unresolved jurisdiction boundary or directory conflict overrides the score and keeps the candidate in `research` or `rejected`.

## Official-statistics path

When usable official statistics exist, rank authorities using the reported measure most aligned with the product's purpose, ordinarily grievance volume or RTI application volume. Record:

- reporting body and official source ID;
- reporting period;
- measure and unit;
- whether the figures cover all authorities or only a subset;
- missing/suppressed values;
- methodological caveats; and
- retrieval and review dates.

Statistics identify candidates; they do not replace the hard directory gates. If the official data measures disposal or pendency, do not relabel it as complaint prevalence.

## Selection process

1. Inventory official statistics and authority directories separately for each jurisdiction.
2. Create a research scorecard conforming to `data/schemas/authority-candidate.schema.json`.
3. Preserve every candidate considered, including rejected candidates and the reason.
4. Rank within the jurisdiction using official statistics where adequate, otherwise the fallback score.
5. Apply hard gates and resolve duplicate, subordinate or overlapping authorities.
6. Select 5–10 candidates with evidence quality taking priority over filling a quota.
7. Convert only verified candidates into `authority.schema.json` records.
8. Obtain technical and legal/RTI directory review before filing-ready status.

If fewer than five authorities pass, the jurisdiction has not met the MVP completion gate and remains research-only. The product must not weaken evidence requirements to meet the numerical target.

## Tie-breaking

For equal totals, prefer in order:

1. higher source completeness;
2. higher grievance relevance;
3. higher maintainability;
4. more recent official evidence; and
5. stable designation-based records over person-named directories.

If still tied, retain both as pending candidates and document the later selection decision rather than making an arbitrary ranking appear objective.

## Review and freshness

- Record the scorecard's `asOfDate`; do not silently recompute historical rankings.
- Recheck selected authority records monthly for URL/checksum changes and before a release.
- Apply the jurisdiction's configured freshness window to authority records.
- A changed directory, missing page, new conflict or expired `staleAfter` date immediately blocks new filing-ready output for the affected authority until reviewed.
- Never automatically copy a changed personal name, address or designation into production data.

## Remaining research

The next step is to collect official statistics and official authority/PIO/FAA directory sources for Central, Delhi, Haryana, Maharashtra and Goa, then publish separate scored candidate tables. No current profile has passed that gate.
