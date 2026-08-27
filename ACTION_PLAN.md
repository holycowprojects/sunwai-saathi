# SunwaiSaathi — MVP Action Plan

**Status:** Active  
**Baseline:** [SPEC.md](./SPEC.md), version 0.1.0  
**Developer and steward:** Holy Cow Studios  
**Project direction and milestone approval:** Akash  
**Delivery model:** Quality-gated; no fixed deadline  
**Cost constraint:** Zero incremental development and operating spend

## 1. How this plan is used

`SPEC.md` is the authoritative product baseline. This file defines the order in which that specification is delivered. `TODO.md` is the operational checklist and must link completed work to evidence.

A material change to scope, legal safety, privacy, cost, architecture, or public commitments requires Akash’s approval and an update to `SPEC.md`. Technical decisions discovered through experiments must be recorded as Architecture Decision Records (ADRs).

## 2. Non-negotiable sequencing rules

1. Do not commit to a framework, OCR library, PDF engine, browser model, hosted AI provider, or production host before the technical spike records comparative evidence.
2. Do not label a jurisdiction or authority filing-ready until its rules, sources, templates, and addresses pass technical and legal/RTI review.
3. Do not allow AI to determine or override jurisdiction, fee, deadline, filing route, authority, address, protected wording, or required caveats.
4. Do not enable any model/provider in production if it produces a critical error in the release evaluation suite.
5. Do not publish a production release until security, accessibility, supported-browser, documentation, and zero-critical-error gates pass.
6. Keep Central Government and Government of NCT of Delhi as independent jurisdiction profiles.
7. Keep the deterministic workflow functional without AI, accounts, analytics, server-side case storage, server-side document uploads, or email reminders.
8. Use downloadable calendar reminders; do not reintroduce server-scheduled reminders without an approved specification change.
9. Preserve the static-first PWA architecture: sensitive processing stays local and hosted capabilities remain optional, explicit, and allowlisted.

## 3. Project-wide definition of done

The public beta is complete only when:

- Central Government, Delhi, Haryana, Maharashtra, and Goa have current, reviewed primary-source provenance.
- Each jurisdiction includes 5–10 selected authorities satisfying the published verification standard.
- English and Hindi protected templates have language and legal/RTI approval.
- Default applications request the focused record bundle; officer information remains a separate, unchecked, reviewed opt-in clause.
- The standard 30-day calculator identifies its date basis and whether the result is confirmed or estimated.
- All six first-appeal outcome categories work through reviewed deterministic modules.
- PDF, JPG, and PNG intake, OCR, redaction, drafting, PDF generation, encryption, and case storage remain local.
- The deterministic PWA workflow operates offline after installation and requires an update before a new filing-ready export when newer legal data exists.
- Submission packs include correct portal text, PDF output, filing guidance, application/legal-data versions, and `.ics` calendar output.
- The public evaluation suite contains zero critical legal errors.
- Every enabled AI configuration passes the complete critical suite with pinned configuration.
- WCAG 2.2 AA checks and focused manual accessibility testing pass.
- Chrome, Edge, Firefox, and Safari automation plus documented manual checks pass.
- The automated security baseline passes.
- Portfolio-grade documentation is complete.
- Production deployment incurs no incremental project cost and follows the protected release workflow.
- Akash approves production promotion.

## 4. Milestone plan

### Milestone 1 — Legal-data verification and product foundation

**Objective:** Convert the frozen product concept into a traceable, primary-source-backed legal-data foundation for all five jurisdictions.

**Prerequisites:** Frozen `SPEC.md`; primary-source-only policy; identified technical and legal/RTI approval roles.

**Workstreams:**

1. Build a primary-source inventory for the RTI Act, DPDP commencement/amendment, Central rules and portal, and Delhi, Haryana, Maharashtra, and Goa rules and portals.
2. Verify statutory constants, effective dates, standard deadlines, first-appeal requirements, fee exemptions, and the precise Section 8(1)(j)/Section 8(2) treatment.
3. Verify per-jurisdiction fees, payment modes, forms, ID/BPL evidence requirements, portal coverage, attachment behavior, text limits, application requirements, first-appeal requirements, and filing routes.
4. Define schemas for legal rules, sources, jurisdictions, authorities, review state, freshness, and versioning.
5. Identify 5–10 candidate authorities per jurisdiction using official evidence; use the documented fallback rubric only when official ranking data is inadequate.
6. Produce supported/unsupported scenario definitions, a legal-review checklist, risk register, and requirement-to-evidence traceability matrix.

**Deliverables:**

- Primary-source inventory and checksums
- Verified statutory constants and change history
- Five jurisdiction research dossiers
- Legal-data, source, jurisdiction, and authority schema proposals
- Authority-selection evidence, scoring rubric, and candidate lists
- Supported/unsupported scenario matrix
- Legal/RTI reviewer checklist
- Milestone risk register
- Requirements traceability matrix

**Verification:**

- Every operative value maps to a primary official source, provision reference, effective date, retrieval date, and checksum.
- Conflicts between official sources are documented and kept out of filing-ready behavior until resolved.
- Central and Delhi rules and portals are independently represented.
- No secondary source controls application behavior.
- All initial legal statements in `SPEC.md` are classified as verified, corrected, disputed, or unsupported.

**Completion gate:** Akash approves the source inventory, supported-case boundary, and schema direction. A designated legal/RTI reviewer approves the legal conclusions or they remain explicitly unreviewed and non-filing-ready.

**Key risks/blockers:** Inaccessible or inconsistent government publications; missing official authority statistics; inability to recruit a qualified volunteer reviewer.

### Milestone 2 — Technical feasibility spike

**Objective:** Select a browser-first implementation stack by proving or rejecting the highest-risk requirements.

**Prerequisite:** Milestone 1 gate passed sufficiently to provide representative English/Hindi rules, templates, and sample documents.

**Workstreams:**

1. Compare candidate stacks and libraries using reproducible fixtures.
2. Prove installable static PWA behavior, deterministic offline operation, legal-data update detection, and filing-ready export blocking.
3. Benchmark local PDF/image parsing, OCR, sensitive-value detection, approved redaction export, and malformed-file handling.
4. Verify English/Hindi font embedding and print-ready PDF consistency.
5. Prototype passphrase-derived encryption, local case storage, deletion, and recovery-failure behavior.
6. Validate `.ics` output across common calendar applications.
7. Benchmark local browser models at or below 500 MB and provider-neutral BYOK adapters.
8. Compare Hostinger with eligible zero-incremental-cost static hosts for PWA behavior, headers, previews, performance, and portability.
9. Test CSP/network allowlisting, supported browsers, bundle size, memory, and WCAG 2.2 AA feasibility.

**Deliverables:** Reproducible spike workspace, technology scorecard, measurements, hosting comparison, AI ship/no-ship evidence, initial threat model, and ADRs selecting the stack and core libraries.

**Verification:** Repeatable commands and fixtures reproduce every published measurement; deterministic fallbacks exist for unsupported AI/OCR/device capabilities.

**Completion gate:** Every critical browser, privacy, security, Hindi-document, and offline risk has a viable implementation or an accepted deterministic fallback. Akash approves material architecture and hosting choices.

**Key risks/blockers:** Hindi OCR/PDF quality, Safari limitations, browser-model accuracy/size, Hostinger header or deployment constraints.

### Milestone 3 — Deterministic drafting core

**Objective:** Implement a framework-independent domain core that produces reviewed RTI content without AI.

**Prerequisite:** Milestone 2 ADRs accepted; Milestone 1 schemas and source conventions approved.

**Workstreams:**

1. Implement validated, versioned jurisdiction/source/authority data.
2. Implement provenance, freshness, stale-warning, and update-required behavior.
3. Implement jurisdiction resolution and strict Central-versus-Delhi separation.
4. Implement English/Hindi protected template modules, focused record bundle, optional officer clause, BPL guidance, and portal-length variants.
5. Implement date-event classification and the standard 30-day deadline calculator.
6. Implement application/legal-data version stamping and deterministic submission-pack data contracts.
7. Add unit, property, fixture, and critical-regression tests.

**Deliverables:** Jurisdiction schema/validator, source provenance tooling, rules engine, reviewed templates, draft composer, date calculator, version stamping, and test suite.

**Verification:** Boundary/date tests, invalid-data tests, stale-data tests, deterministic snapshots, English/Hindi semantic review, and zero critical errors in deterministic fixtures.

**Completion gate:** Technical and legal/RTI reviewers approve the rules and protected templates; deterministic fixtures have zero critical errors.

**Key risks/blockers:** Template wording review delays; discrepancies between portal and Gazette requirements; overly coupled UI/domain design.

### Milestone 4 — Citizen PWA workflow

**Objective:** Deliver the anonymous, accessible, privacy-first drafting and submission-pack experience.

**Prerequisite:** Stable deterministic core and accepted PWA/document ADRs.

**Workstreams:**

1. Build onboarding, independence/not-legal-advice notice, citizenship confirmation, and supported-case guardrails.
2. Build guided intake, jurisdiction resolution, BPL selection, date-event selection, and mandatory confirmation for critical fields.
3. Build local PDF/JPG/PNG validation, parsing, OCR, sensitive-value warnings, redaction preview, and manual fallback.
4. Build structured editing that protects legal clauses and deterministic values.
5. Generate portal-ready text, print-ready PDF, filing instructions, provenance guidance, version summary, and `.ics` reminder.
6. Add opt-in passphrase-encrypted local case saving, deletion, and shared-device warnings.
7. Implement installable/offline PWA behavior and legal-data update blocking.
8. Complete responsive, keyboard, screen-reader, scaling, contrast, focus, validation, and reduced-motion behavior.

**Deliverables:** End-to-end deterministic PWA, local document pipeline, output pack, calendar export, encrypted local saving, accessible UI, and browser tests.

**Verification:** Playwright across Chrome/Edge-compatible Chromium, Firefox, and WebKit; manual Holy Cow Studios device scenarios; offline/update tests; privacy-boundary tests; WCAG automation and focused manual checks.

**Completion gate:** Automated acceptance and internal manual scenarios pass with no server case/document transmission and no critical drafting error.

**Key risks/blockers:** Browser storage loss, large OCR assets, print differences, false-positive redaction, and first-time-user confusion from internal-only testing.

### Milestone 5 — First-appeal workflow

**Objective:** Generate reviewed first-appeal packs for all six approved outcome categories.

**Prerequisite:** Citizen PWA and deterministic document pipeline stable; verified FAA data available for supported authorities.

**Workstreams:**

1. Add no-response, incomplete, incorrect/misleading, refusal, excessive-fee, and other-issue intake branches.
2. Process uploaded PIO responses locally and suggest dates, provisions, and categories with mandatory user confirmation.
3. Implement modular reviewed appeal grounds; prevent unrestricted AI-generated legal arguments.
4. Resolve FAA office/designation/address and block filing-ready status when address evidence is insufficient.
5. Generate first-appeal portal text, PDF, instructions, versions, and attachment checklist.

**Deliverables:** Six deterministic appeal modules, response extraction flow, FAA lookup behavior, appeal submission pack, and branch-complete evaluations.

**Verification:** Every outcome across every jurisdiction, missing/uncertain response fields, unverified FAA data, English/Hindi consistency, malformed uploads, and zero critical appeal errors.

**Completion gate:** All first-appeal branches pass the critical suite and required templates receive technical, language, and legal/RTI approval.

**Key risks/blockers:** State-specific appeal forms/fees, over-classification of PIO replies, insufficient FAA source coverage.

### Milestone 6 — AI assistance and public evaluations

**Objective:** Add optional, constrained AI extraction and publish a reproducible safety benchmark.

**Prerequisite:** Deterministic form and extraction fallback complete; stable structured schemas and critical-error definitions.

**Workstreams:**

1. Build a provider-neutral adapter and memory-only BYOK boundary.
2. Benchmark eligible hosted providers for English/Hindi extraction, schema validity, latency, privacy constraints, pinning, and zero-incremental-cost compatibility.
3. Benchmark local models at or below 500 MB; ship none if every critical case does not pass.
4. Create at least 20–30 expert-reviewed synthetic scenarios across all jurisdictions and workflow branches.
5. Implement the safety-weighted grader and publish cases, expected outputs, grading, configurations, results, and limitations.
6. Add model cards and require full re-evaluation for any model, prompt, quantization, schema, or adapter change.

**Deliverables:** AI adapter, provider benchmark, approved BYOK integration if one qualifies, local-model decision, public benchmark, grader, reports, and model cards.

**Verification:** Schema fuzzing, prompt-injection fixtures, deterministic-conflict tests, Hindi/English parity, memory-only secret tests, and zero critical errors for every production configuration.

**Completion gate:** No enabled AI configuration has a critical failure. Failed configurations remain developer-only or are excluded while their results may be published.

**Key risks/blockers:** Provider version drift, inability to pin models, local-model quality, browser memory limits, API-key exposure through third-party libraries.

### Milestone 7 — Public beta release

**Objective:** Publish a safe, documented, zero-incremental-cost beta through a protected release process.

**Prerequisite:** All earlier milestone gates and the project-wide definition of done pass.

**Workstreams:**

1. Finalize all five reviewed jurisdiction profiles and 5–10 verified authorities per jurisdiction.
2. Complete README, architecture, ADRs, threat model, privacy notice, legal-data methodology, evaluation report, model cards, accessibility statement, contribution guide, security policy, deployment guide, user guide, limitations, changelog, and notices.
3. Configure repository governance, DCO enforcement, issue templates, private security reporting, protected branches, CI, and preview deployment.
4. Complete security, accessibility, browser, offline, performance, privacy, and critical legal evaluation reports.
5. Validate the selected Holy Cow Studios subdomain/host, CSP, update flow, rollback procedure, and zero-incremental-cost constraint.
6. Tag the release, generate the changelog, and deliberately promote the approved build.

**Deliverables:** Public monorepo, production PWA, complete documentation/evidence, tagged release, changelog, and feedback workflows.

**Verification:** Clean-build reproduction; release-artifact checksum; production smoke tests; source/version visibility; no analytics/server case storage; rollback rehearsal; all gates linked from the release record.

**Completion gate:** Akash approves production promotion after every Section 26 completion criterion in `SPEC.md` is evidenced.

**Key risks/blockers:** External legal review availability, official-source changes near release, hosting constraints, incomplete Hindi review, or a critical regression.

## 5. Immediate Milestone 1 execution order

1. Create the source inventory format and legal-claim status vocabulary.
2. Verify national RTI/DPDP provisions and their commencement history.
3. Research Central, Delhi, Haryana, Maharashtra, and Goa in parallel as independent dossiers.
4. Resolve official-source conflicts before encoding values.
5. Draft and validate legal-data/source/jurisdiction/authority schemas against all five dossiers.
6. Rank launch authorities from official evidence and apply the fallback rubric where necessary.
7. Build the supported-case matrix, reviewer checklist, risk register, and traceability matrix.
8. Run technical consistency review, then obtain designated legal/RTI review.
9. Present the complete Milestone 1 evidence package to Akash for approval.
