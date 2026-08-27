# SunwaiSaathi — Project TODO

**Authoritative baseline:** [SPEC.md](./SPEC.md)  
**Execution plan:** [ACTION_PLAN.md](./ACTION_PLAN.md)  
**Current phase:** Milestone 1 — Legal-data verification and product foundation

## Status and maintenance rules

- `[ ]` Pending
- `[x]` Completed
- Blocked tasks remain unchecked and include `BLOCKED: <reason>`.
- A completed research, legal, evaluation, security, or release task must link to its evidence.
- Do not mark a milestone complete until its gate is approved.
- Material scope changes require an approved `SPEC.md` update.
- Framework, provider, model, host, and major library decisions wait for Milestone 2 evidence.

## Project foundation

- [x] Complete product discovery and freeze the MVP baseline in [SPEC.md](./SPEC.md).
- [x] Confirm product name `SunwaiSaathi` and repository name `sunwai-saathi`.
- [x] Confirm Holy Cow Studios as developer, steward, and copyright holder.
- [x] Confirm Akash as project director and milestone approver.
- [x] Confirm Apache-2.0 licensing and DCO contribution model.
- [x] Confirm zero-incremental-cost constraint and Hostinger as a hosting candidate.
- [x] Confirm the static-first PWA and local-processing architecture.
- [x] Confirm downloadable calendar reminders instead of email reminders.
- [x] Create the milestone action plan in [ACTION_PLAN.md](./ACTION_PLAN.md).
- [x] Create this operational checklist.

## Milestone 1 — Legal-data verification and product foundation

### Research framework

- [x] Define the primary-source inventory template in [SOURCE_INVENTORY.md](./docs/legal-data/SOURCE_INVENTORY.md).
- [x] Define legal-claim statuses: unverified, verified, corrected, disputed, unsupported, superseded.
- [x] Define citation, retrieval-date, effective-date, provision-reference, and checksum conventions.
- [x] Define conflict-handling rules for inconsistent official sources.
- [x] Create separate research dossiers for Central, Delhi, Haryana, Maharashtra, and Goa.

### National statutory baseline

- [ ] Verify RTI Act Section 6(1) text and product implications.
- [ ] Verify RTI Act Section 7(1) standard response period and receipt basis.
- [ ] Verify RTI Act Sections 19(1), 19(3), and 19(6) appeal periods and requirements.
- [ ] Verify RTI Act Section 7(6) delayed-information fee rule.
- [ ] Document Section 6(3) transfer behavior as unsupported deadline scope for MVP.
- [ ] Verify the DPDP Act Section 44(3) commencement notification and exact effective date.
- [ ] Verify the amended RTI Act Section 8(1)(j) text.
- [ ] Verify the continued Section 8(2) text and prevent categorical overstatement.
- [ ] Draft the officer-information opt-in caveat for expert review.
- [ ] Create a national statutory change-history record.

### Central Government dossier

- [ ] Verify application fee and BPL exemption/evidence requirements.
- [ ] Verify accepted online and offline payment methods.
- [ ] Verify portal scope, excluded authorities, attachment support, and text limits.
- [ ] Verify application and first-appeal filing routes and forms.
- [ ] Verify first-appeal fee and evidence requirements.
- [ ] Record official authority/PIO/FAA directory sources.
- [ ] Record source metadata, provisions, effective dates, and checksums.
- [ ] Classify the Central profile as reviewed or non-filing-ready.

### Government of NCT of Delhi dossier

- [ ] Verify Delhi’s separation from the Central RTI portal and identify official filing routes.
- [ ] Verify application fee and BPL exemption/evidence requirements.
- [ ] Verify payment methods, prescribed form, attachments, and text limits.
- [ ] Verify first-appeal fee, form, filing route, and evidence requirements.
- [ ] Record official authority/PIO/FAA directory sources.
- [ ] Record source metadata, provisions, effective dates, and checksums.
- [ ] Classify the Delhi profile as reviewed or non-filing-ready.

### Haryana dossier

- [ ] Verify application fee and BPL exemption/evidence requirements.
- [ ] Verify online/offline payment methods and portal coverage.
- [ ] Verify prescribed form, attachments, text limits, and identity requirements.
- [ ] Verify first-appeal fee, form, filing route, and evidence requirements.
- [ ] Record official authority/PIO/FAA directory sources.
- [ ] Record source metadata, provisions, effective dates, and checksums.
- [ ] Classify the Haryana profile as reviewed or non-filing-ready.

### Maharashtra dossier

- [ ] Verify the operative Maharashtra RTI Rules and effective date as of the research date.
- [ ] Verify application fee and BPL exemption/evidence requirements.
- [ ] Verify online/offline payment methods and portal coverage.
- [ ] Verify prescribed application format, word/text limits, attachments, and proof-of-identity requirement.
- [ ] Verify first-appeal fee, form, filing route, and evidence requirements.
- [ ] Record official authority/PIO/FAA directory sources.
- [ ] Record source metadata, provisions, effective dates, and checksums.
- [ ] Classify the Maharashtra profile as reviewed or non-filing-ready.

### Goa dossier

- [ ] Verify application fee and BPL exemption/evidence requirements.
- [ ] Verify online/offline payment methods and portal coverage.
- [ ] Verify prescribed form, attachments, text limits, and identity requirements.
- [ ] Verify first-appeal fee, form, filing route, and evidence requirements.
- [ ] Record official authority/PIO/FAA directory sources.
- [ ] Record source metadata, provisions, effective dates, and checksums.
- [ ] Classify the Goa profile as reviewed or non-filing-ready.

### Legal-data design

- [x] Define the initial [source-provenance schema](./data/schemas/source.schema.json).
- [ ] Define the legal-rule schema with effective and review dates.
- [x] Define the initial independent [jurisdiction profile schema](./data/schemas/jurisdiction.schema.json).
- [ ] Define authority/PIO/FAA office-and-designation schema without personal officer names.
- [ ] Define reviewed, stale, unsupported, and filing-ready state semantics.
- [ ] Define separate application and legal-data version formats.
- [ ] Validate schemas against all five jurisdiction dossiers.
- [ ] Define monthly source-health and checksum-change outputs.

### Authority selection

- [ ] Collect official grievance/RTI statistics for each jurisdiction.
- [ ] Define the fallback scoring rubric: population served, grievance relevance, source completeness, filing accessibility, maintainability.
- [ ] Produce a scored candidate list for Central Government.
- [ ] Produce a scored candidate list for Delhi.
- [ ] Produce a scored candidate list for Haryana.
- [ ] Produce a scored candidate list for Maharashtra.
- [ ] Produce a scored candidate list for Goa.
- [ ] Select 5–10 launch candidates per jurisdiction, subject to verification.
- [ ] Confirm every selected authority has an official source and maintainable directory path.

### Safety, review, and traceability

- [x] Create the [supported/unsupported scenario matrix](./docs/product/SUPPORTED_CASES.md).
- [ ] Define standard 30-day confirmed-versus-estimated deadline behavior.
- [ ] Document exceptional deadline cases as detected but unsupported.
- [ ] Define the six first-appeal outcome categories and required official inputs.
- [x] Create the [legal/RTI reviewer checklist](./docs/legal-data/REVIEW_CHECKLIST.md).
- [ ] Identify and confirm a volunteer legal/RTI reviewer.
- [ ] Identify and confirm a proficient Hindi reviewer.
- [x] Create the [Milestone 1 risk register](./docs/risk/MILESTONE_1_RISKS.md).
- [x] Create the initial [requirement-to-source-and-test traceability matrix](./docs/product/TRACEABILITY.md).
- [ ] Classify every initial legal claim in `SPEC.md`.
- [ ] Complete technical consistency review.
- [ ] Complete designated legal/RTI review.
- [ ] Obtain Akash’s Milestone 1 approval.

## Milestone 2 — Technical feasibility spike

- [ ] Define representative English/Hindi documents, rules, and test fixtures.
- [ ] Select candidate stacks and libraries for comparison without committing to one.
- [ ] Prove installable static PWA behavior.
- [ ] Prove complete deterministic offline workflow after first load.
- [ ] Prove legal-data update notification and filing-ready export blocking.
- [ ] Benchmark local PDF/JPG/PNG validation, parsing, and OCR.
- [ ] Test malformed, oversized, mislabeled, and adversarial document fixtures.
- [ ] Benchmark sensitive-value detection and user-approved redaction export.
- [ ] Verify English/Hindi font embedding and print consistency.
- [ ] Prototype passphrase-derived encryption, local storage, deletion, and wrong-passphrase handling.
- [ ] Validate `.ics` files in representative calendar applications.
- [ ] Benchmark browser models at or below 500 MB.
- [ ] Make and document the public local-AI ship/no-ship decision.
- [ ] Prototype provider-neutral, memory-only BYOK adapters.
- [ ] Compare eligible AI providers using the approved benchmark criteria.
- [ ] Test strict CSP and explicit-action network allowlisting.
- [ ] Benchmark bundle size, load time, memory use, and low-connectivity behavior.
- [ ] Test Chrome, Edge, Firefox, and Safari capability/fallback behavior.
- [ ] Evaluate WCAG 2.2 AA feasibility.
- [ ] Compare Hostinger and eligible zero-incremental-cost static hosting options.
- [ ] Create initial threat model.
- [ ] Publish technology scorecard and reproducible experiment commands.
- [ ] Record stack, library, hosting, and fallback ADRs.
- [ ] Obtain Akash’s approval for material architecture choices.
- [ ] Pass the Milestone 2 gate.

## Milestone 3 — Deterministic drafting core

- [ ] Scaffold the selected monorepo and toolchain.
- [ ] Add Apache-2.0 `LICENSE`, Holy Cow Studios `NOTICE`, and attribution.
- [ ] Implement source, legal-rule, jurisdiction, and authority schemas.
- [ ] Implement schema and cross-record validation.
- [ ] Implement application/legal-data versioning.
- [ ] Implement provenance, source checksum, and freshness state handling.
- [ ] Implement stale warning and acknowledgement behavior.
- [ ] Implement strict Central-versus-Delhi jurisdiction resolution.
- [ ] Encode reviewed profiles for all five jurisdictions.
- [ ] Encode verified launch authority entries without personal officer names.
- [ ] Implement focused record-bundle composer.
- [ ] Implement separate unchecked officer-information clause.
- [ ] Implement BPL guidance behavior.
- [ ] Implement portal-ready text and full-attachment variants.
- [ ] Implement protected English templates.
- [ ] Implement protected Hindi templates.
- [ ] Obtain Hindi and legal/RTI template approvals.
- [ ] Implement date-event classification and standard 30-day calculation.
- [ ] Implement confirmed/estimated result labeling.
- [ ] Implement deterministic submission-pack data contract.
- [ ] Add unit, boundary, property, invalid-data, stale-data, and snapshot tests.
- [ ] Achieve zero critical errors in deterministic fixtures.
- [ ] Pass the Milestone 3 gate.

## Milestone 4 — Citizen PWA workflow

- [ ] Build beta, independence, privacy, and not-legal-advice onboarding.
- [ ] Add Indian-citizenship confirmation without proof collection.
- [ ] Build guided intake for grievance, authority, dates, address, language, and BPL status.
- [ ] Build supported-case detection and safe unsupported-case exit.
- [ ] Build jurisdiction resolution with mandatory confirmation for uncertainty.
- [ ] Build local PDF/JPG/PNG validation and parsing.
- [ ] Build local OCR with manual fallback.
- [ ] Build local sensitive-value warning and redaction preview.
- [ ] Preserve original files and export only user-approved redacted copies.
- [ ] Build structured editing with protected legal content.
- [ ] Build portal-ready text and print-ready English/Hindi PDF output.
- [ ] Build filing instructions, source/freshness guidance, and version summary.
- [ ] Build `.ics` calendar reminder export.
- [ ] Build optional passphrase-encrypted local case saving.
- [ ] Add wrong-passphrase, delete-case, and shared-device behavior.
- [ ] Implement installable and offline PWA behavior.
- [ ] Implement new-legal-data update requirement before filing-ready export.
- [ ] Implement WCAG 2.2 AA interaction and content requirements.
- [ ] Add Playwright coverage for Chromium, Firefox, and WebKit.
- [ ] Run manual Holy Cow Studios device and role scenarios.
- [ ] Verify no case/document transmission or analytics.
- [ ] Pass the Milestone 4 gate.

## Milestone 5 — First-appeal workflow

- [ ] Build no-response appeal intake and reviewed grounds.
- [ ] Build incomplete-information appeal intake and reviewed grounds.
- [ ] Build incorrect/misleading-information appeal intake and reviewed grounds.
- [ ] Build refusal appeal intake and reviewed grounds.
- [ ] Build excessive-fee appeal intake and reviewed grounds.
- [ ] Build other-issue intake using reviewed bounded modules.
- [ ] Build local PIO-response upload and extraction.
- [ ] Require confirmation of every suggested date, provision, and category.
- [ ] Implement verified FAA lookup and non-filing-ready fallback.
- [ ] Build English/Hindi first-appeal portal text and PDF packs.
- [ ] Add first-appeal attachment and filing guidance.
- [ ] Test every outcome across every jurisdiction.
- [ ] Test unverified FAA, malformed upload, and uncertain extraction paths.
- [ ] Obtain legal/RTI and Hindi approvals.
- [ ] Achieve zero critical first-appeal errors.
- [ ] Pass the Milestone 5 gate.

## Milestone 6 — AI assistance and public evaluations

- [ ] Implement provider-neutral structured extraction interface.
- [ ] Implement memory-only API-key handling.
- [ ] Verify keys never enter storage, logs, diagnostics, or exports.
- [ ] Benchmark eligible hosted providers with pinned configurations.
- [ ] Select at most one production BYOK provider integration initially.
- [ ] Benchmark eligible local models at or below 500 MB.
- [ ] Exclude local AI from production if no candidate passes all critical cases.
- [ ] Create at least 20–30 expert-reviewed synthetic scenarios.
- [ ] Cover all five jurisdictions and six appeal outcome categories.
- [ ] Include DPDP/officer-caveat and AI-versus-rule conflict cases.
- [ ] Implement safety-weighted field scoring.
- [ ] Define and enforce the zero-critical-error release gate.
- [ ] Add schema, prompt-injection, Hindi/English parity, and model-drift tests.
- [ ] Publish cases, expected outputs, grader, configurations, results, and limitations.
- [ ] Publish model cards for every enabled configuration.
- [ ] Require full evaluation after model, prompt, quantization, schema, or adapter changes.
- [ ] Pass the Milestone 6 gate.

## Milestone 7 — Public beta release

- [ ] Confirm all five jurisdiction profiles are current and reviewed.
- [ ] Confirm 5–10 verified launch authorities per jurisdiction.
- [ ] Complete README and product/user documentation.
- [ ] Complete architecture overview and ADR index.
- [ ] Complete threat model and privacy notice.
- [ ] Complete legal-data methodology and support matrix.
- [ ] Complete evaluation report and model cards.
- [ ] Complete accessibility statement and test evidence.
- [ ] Complete contribution guide, Code of Conduct, DCO instructions, and security policy.
- [ ] Complete deployment guide, changelog, and known-limitations register.
- [ ] Add structured GitHub issue templates with personal-data warnings.
- [ ] Configure private security reporting.
- [ ] Configure protected branches, required CI, preview deployment, tags, and deliberate production promotion.
- [ ] Run dependency, secret, static-analysis, CSP, hostile-file, cryptography, and privacy-boundary checks.
- [ ] Run supported-browser, offline/update, performance, and accessibility release suites.
- [ ] Run the full legal and AI critical-error suite.
- [ ] Confirm no analytics, accounts, server case storage, server document upload, or email reminder service.
- [ ] Validate selected host/subdomain and zero-incremental-cost operation.
- [ ] Validate production CSP, update behavior, and rollback procedure.
- [ ] Produce signed/tagged release and generated changelog.
- [ ] Obtain Akash’s production approval.
- [ ] Deliberately promote the approved release.
- [ ] Run production smoke tests and link evidence from the release record.

## Recurring maintenance

### Monthly legal/source health

- [ ] Run official-source URL health checks.
- [ ] Detect and review source checksum changes.
- [ ] Review rules approaching or exceeding six months since verification.
- [ ] Open tracked issues for broken, changed, or stale sources.
- [ ] Reclassify affected filing-ready profiles when evidence is insufficient.

### Dependency and security maintenance

- [ ] Review dependency and secret-scanning results.
- [ ] Review security advisories affecting parsing, PDF, OCR, PWA, storage, or cryptography.
- [ ] Re-run hostile-file and privacy-boundary regression tests after relevant changes.
- [ ] Confirm CSP allowlist and production network behavior remain minimal.

### Evaluation maintenance

- [ ] Run the complete deterministic and AI release suites after relevant changes.
- [ ] Re-evaluate every model/provider configuration after any pinned component changes.
- [ ] Publish updated benchmark results and limitations.
- [ ] Reject production promotion on any critical failure.

### Accessibility and compatibility maintenance

- [ ] Run automated accessibility and supported-browser regression checks.
- [ ] Perform focused manual keyboard and screen-reader checks before releases.
- [ ] Review community device compatibility reports.
- [ ] Record and triage regressions with evidence.

### Documentation and governance maintenance

- [ ] Update changelog, ADRs, support matrix, and known limitations with each release.
- [ ] Verify completed TODO items link to durable evidence.
- [ ] Review contribution, security, privacy, and legal-data policies after material changes.
- [ ] Keep post-beta ideas out of MVP work unless `SPEC.md` is formally updated.

## Post-beta recommendations — not MVP tasks

- [ ] Conduct external usability research with citizens and NGO/RTI volunteers.
- [ ] Evaluate additional jurisdictions through the same primary-source and review process.
- [ ] Consider second-appeal drafting only after verified commission-specific data exists.
- [ ] Consider portable encrypted case-file export.
- [ ] Consider additional reviewed languages.
