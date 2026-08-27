# SunwaiSaathi — MVP Product and Engineering Specification

**Status:** Frozen MVP baseline  
**Specification version:** 0.1.0  
**Date:** 27 August 2026  
**Product:** SunwaiSaathi  
**Repository:** `sunwai-saathi`  
**Developer and steward:** Holy Cow Studios  
**Project direction:** Akash  
**Development attribution:** Developed and maintained by Holy Cow Studios, directed by Akash, with AI-assisted engineering using OpenAI Codex.  
**License:** Apache License 2.0  
**Copyright:** Copyright © 2026 Holy Cow Studios

## 1. Purpose

SunwaiSaathi is a privacy-first, open-source Progressive Web App that helps Indian citizens and NGO volunteers prepare Right to Information (RTI) applications about unresolved government grievances.

The MVP focuses on obtaining existing government records about a grievance rather than asking the authority to resolve the grievance or generate explanations. Its default records request covers certified copies of:

- the action-taken report;
- file notings;
- file-movement records;
- relevant orders; and
- correspondence concerning the identified grievance.

SunwaiSaathi provides informational drafting assistance and is not a law firm, legal representative, filing agent, government service, or source of legal advice. It does not submit applications or appeals and does not collect payments.

## 2. Portfolio objective

The project primarily demonstrates:

1. applied AI engineering; and
2. AI evaluation engineering.

The central engineering proposition is that AI may assist with extraction and organization, but it must never recall, infer, or override legally operative rules. Jurisdiction, fees, deadlines, filing routes, prescribed requirements, protected template clauses, and mandatory warnings come from reviewed, versioned, deterministic data.

## 3. Release objective

The first release is a publicly usable beta. It must:

- use verified primary official sources;
- clearly identify its beta status and limitations;
- operate without requiring an account;
- remain useful without AI;
- cost no additional money to develop or operate;
- avoid transmitting case content in the deterministic workflow;
- meet the release gates in this specification; and
- distinguish reviewed, filing-ready behavior from unverified or unsupported behavior.

The MVP advances by quality gates rather than a fixed deadline.

## 4. Users

The primary users are:

- citizens following up on unresolved government grievances; and
- NGO or civic-help volunteers assisting citizens.

Both groups use the same workflow. The MVP does not include NGO workspaces, organization accounts, teams, role-based access, shared cases, assignments, or volunteer-specific case management.

## 5. Supported jurisdictions

The MVP covers five independent jurisdiction profiles:

1. Central Government;
2. Government of NCT of Delhi;
3. Haryana;
4. Maharashtra; and
5. Goa.

Central Government and Government of NCT of Delhi must never be treated as the same filing jurisdiction. Each profile independently versions its rules, filing route, portal coverage, fees, payment methods, forms, attachments, authority sources, and first-appeal requirements.

Jurisdictions may be delivered incrementally behind validation status flags even though all five are included in MVP scope.

## 6. Explicitly excluded from MVP

The following are out of scope:

- jurisdictions other than the five listed above;
- general-purpose RTI drafting unrelated to an existing grievance;
- automatic filing or browser-assisted submission;
- collection or processing of RTI fees;
- second-appeal drafting;
- second-appeal disposal-time estimates;
- exceptional deadline workflows, including life-or-liberty, APIO, transfer, third-party consultation, exempt-organization, and additional-fee timing variations;
- officer names as directory data;
- accounts and cloud case storage;
- email reminders;
- server-side document processing;
- organization workspaces;
- analytics or background telemetry;
- unrestricted AI-authored legal arguments; and
- live scraping or AI inference of legal rules, PIOs, FAAs, or addresses.

Unsupported and exceptional cases must receive a clear explanation rather than a potentially incorrect draft or deadline.

## 7. Core product principles

### 7.1 Records, not grievance resolution

The product requests existing, identifiable records. It must avoid presenting RTI as a mechanism that compels the authority to solve the underlying grievance, answer open-ended “why” questions, create new information, give opinions, or promise a fast outcome.

### 7.2 Deterministic law

Legal behavior is sourced from reviewed data and protected templates. AI cannot override it, even when the AI result has high confidence.

### 7.3 Jurisdiction-aware behavior

There is no universal state configuration. Every fee, payment mode, portal link, character limit, form requirement, attachment rule, and appeal requirement is selected from the resolved jurisdiction profile.

### 7.4 Privacy by architecture

The core application is static and local-first. Documents, case facts, generated drafts, addresses, passphrases, and local AI activity remain on the user’s device unless the user deliberately invokes an allowed hosted AI provider.

### 7.5 Honest limitations

The UI must clearly state what is supported, what is estimated, which date event was used, when data was reviewed, and when expert help or independent verification is appropriate.

### 7.6 AI-assisted, not AI-led

The citizen-facing promise is reliable RTI drafting. AI is optional convenience for document extraction and non-binding suggestions, not the legal authority or primary product claim.

## 8. Legal baseline and verification requirements

The following items are initial research findings, not yet approved legal data. Milestone 1 must verify them against primary official sources and record the exact operative text, dates, and source checksums:

- RTI Act Section 6(1): written or electronic request to the appropriate PIO with the prescribed fee.
- RTI Act Section 7(1): standard response period of 30 days from receipt.
- RTI Act Section 19(1): first appeal following lapse or dissatisfaction, subject to the statutory filing period.
- RTI Act Section 19(6): first-appeal disposal within 30 days, extendable to 45 days with the applicable requirement.
- RTI Act Section 19(3): second-appeal filing period, although second-appeal drafting is outside MVP.
- RTI Act Section 7(6): information supplied free of charge when the public authority fails to comply with the applicable time limit, where applicable.
- RTI Act Section 6(3): transfer provisions, for explanation and future design only; transfer timing is outside the MVP deadline calculator.
- DPDP Act Section 44(3) amendment to RTI Act Section 8(1)(j), commenced by notification on the Gazette publication date in November 2025.
- The continued text and possible relevance of RTI Act Section 8(2) must be represented accurately. The product must not make the categorical claim that every public-interest balancing mechanism was removed.

No proposition becomes product behavior merely because it appears in this section.

### 8.1 Officer-information clause

An officer-information request is:

- a separate opt-in clause;
- unchecked by default;
- never silently inserted by AI;
- accompanied by a concise, reviewed warning concerning amended Section 8(1)(j) and unsettled interpretation; and
- not described as inevitably disclosable or inevitably exempt.

The authority directory stores offices and official designations, not individual officer names.

### 8.2 Primary-source policy

Binding behavior may use only primary official sources, including as applicable:

- Gazette notifications;
- India Code;
- official legislation and rules;
- official government portals and circulars; and
- official Information Commission publications.

Secondary sources cannot determine fees, deadlines, filing requirements, portal behavior, authority details, or template clauses. If an operational claim lacks adequate official evidence, the product omits it.

### 8.3 Provenance record

Each legal or jurisdiction rule must record at least:

- stable rule identifier;
- jurisdiction;
- rule category;
- value and units;
- effective-from date;
- effective-to date, if known;
- source title;
- issuing authority;
- source URL;
- retrieval date;
- publication date;
- effective date;
- source-file checksum;
- relevant section, rule, page, or provision reference;
- a short necessary excerpt when legally permissible;
- review status;
- reviewed-at date;
- technical reviewer; and
- designated legal/RTI reviewer.

Complete government documents are not routinely copied into the repository. Metadata, checksums, provision references, and short permitted excerpts protect against link rot and silent replacement.

### 8.4 Freshness

- Data older than six months since review is marked stale.
- Stale data may continue to generate a draft only after a prominent warning and explicit acknowledgement.
- The interface and output show the last-reviewed date and legal-data version.
- Monthly automation checks source health, checksum changes, expiry dates, and schema validity.
- The same checks run whenever legal data changes through a pull request.
- A newer legal-data release blocks production of a new filing-ready export until an installed PWA refreshes. Drafting may continue, and existing packs retain their original recorded version.

### 8.5 Review and merging

Anyone may propose a legal-data change through GitHub. A change affecting legal behavior or templates may merge only when:

- automated schema, source, date, and regression checks pass;
- a technical maintainer approves it; and
- a designated legal/RTI reviewer approves it.

An urgent, clearly harmful legal error uses an expedited hotfix process but still requires both approvals and passing tests.

## 9. Authority directory

The launch directory targets 5–10 high-demand authorities per jurisdiction.

Authority selection is evidence-led using current official grievance statistics, RTI reports, or department publications. When official ranking data is insufficient, use a documented scoring rubric based on:

- population served;
- relevance to unresolved grievances;
- source completeness;
- availability and clarity of filing routes; and
- ongoing maintainability.

Each authority entry should include:

- jurisdiction and authority identifiers;
- official authority name;
- authority type;
- verified PIO office/designation where available;
- verified FAA office/designation where available;
- postal address only when current and officially verified;
- official directory or authority source;
- applicable portal and its coverage constraints;
- last-reviewed date; and
- validation status.

If a postal address cannot be verified, SunwaiSaathi must not generate a filing-ready postal address. It provides a generic draft and directs the user to the official directory. AI cannot infer an address.

## 10. User journey

### 10.1 Onboarding

The user sees:

- beta status;
- independence from government;
- informational-assistance/not-legal-advice notice;
- supported jurisdictions and cases;
- local-processing and privacy summary; and
- a required confirmation that the applicant is an Indian citizen, without identity evidence collection.

### 10.2 Intake

The default path is a guided form. Optional document upload assists with entry.

Expected fields include:

- jurisdiction;
- grievance portal or filing channel;
- grievance reference number;
- grievance filing date;
- responsible public authority or department;
- concise grievance subject;
- relevant record period;
- applicant name;
- complete correspondence address;
- selected application language;
- BPL status; and
- known RTI timing event where applicable.

The user’s complete address is processed locally, included in the application, and included in local storage only if the user explicitly saves an encrypted case.

### 10.3 Upload and extraction

Accepted MVP formats:

- PDF;
- JPG; and
- PNG.

Files are subject to client-side type, size, and page-count limits to be selected in the technical spike. Files are processed locally in the browser by default and are never sent to a SunwaiSaathi server.

Local extraction may suggest fields. Every extracted value must be presented for confirmation. Low-confidence or critical fields require correction or explicit confirmation before drafting. Unsupported devices fall back to manual entry.

### 10.4 Sensitive-information assistance

The application locally detects likely sensitive values, including Aadhaar, PAN, phone numbers, email addresses, postal addresses, and account numbers. It warns the user and offers a local redaction preview.

- No redaction is applied without user approval.
- The original file remains unchanged.
- Redaction creates a separate export copy.
- Automated detection is described as assistance, not a guarantee.

### 10.5 Draft composition

The default focused record bundle requests certified copies of action-taken records, file notings, movement records, relevant orders, and correspondence tied to the grievance.

Users receive structured editing. They may correct facts, dates, authority details, and optional selections, but protected legal text, warnings, and deterministic rule values cannot be freely edited.

The user selects English or Hindi output. English and Hindi use independently reviewed templates; the application does not live-translate protected legal language.

### 10.6 BPL handling

The guided form includes a BPL option. When selected, the product shows the officially verified jurisdiction-specific fee exemption and evidence requirements. SunwaiSaathi does not upload, store, process, or verify BPL proof.

### 10.7 Output

The complete submission pack contains:

- structured final preview;
- concise portal-ready text;
- print-ready PDF application;
- full PDF attachment where the verified portal permits it;
- verified filing instructions;
- official filing links;
- fee and payment guidance;
- legal-data and application versions;
- source and freshness summary outside the application;
- calculated deadline information; and
- downloadable calendar reminder.

The RTI application itself remains concise. Legal citations, provenance details, caveats, and the product disclaimer appear in separate user guidance rather than cluttering the submitted request.

Where a verified portal has a character limit and accepts attachments, generate both concise field text within the limit and the complete PDF. Never assume that a portal accepts attachments.

Generated print documents contain a blank signature line. SunwaiSaathi does not capture drawn or uploaded signatures.

### 10.8 Filing

The product provides official links and verified instructions only. It does not:

- submit forms;
- fill external portal fields;
- initiate payment;
- receive money; or
- represent the applicant.

## 11. Deadline calculation and calendar reminders

The MVP supports the standard 30-day case only.

The user selects the known event:

- application submission;
- portal acknowledgement/receipt; or
- confirmed postal delivery/receipt.

The UI explains which event was used and labels the resulting deadline as confirmed or estimated. The calculator must not silently treat application creation as receipt.

The product generates a downloadable `.ics` calendar reminder. No email reminders, server schedules, reminder tokens, or reminder metadata are used.

## 12. First-appeal workflow

The user explicitly selects what occurred:

- no response;
- incomplete information;
- incorrect or misleading information;
- refusal;
- excessive fee; or
- another issue.

All six categories are in MVP scope. Each uses modular, pre-reviewed grounds. The language model cannot invent unsupported legal grounds.

The user may upload a PIO response as PDF, JPG, or PNG. It is processed locally. Extraction may suggest:

- response date;
- cited statutory provisions;
- decision category; and
- possible issue categories.

The user must confirm every suggestion. The product never decides that an appeal is appropriate on the user’s behalf.

The appeal output uses only verified FAA office/designation and address data. When an FAA address is not verified, the output cannot be labeled filing-ready.

## 13. Local case storage

No account is required. Optional local saving is disabled until the user explicitly chooses it.

Saved case data:

- remains in the browser;
- is encrypted with a key derived from a user-created passphrase;
- is never recoverable by Holy Cow Studios;
- includes only user-confirmed structured fields and needed workflow state;
- does not automatically retain uploaded files, AI prompts, AI responses, or debugging traces; and
- can be deleted through a clear control.

The passphrase and encryption key never leave the device. Forgotten passphrases cannot be recovered. Shared-device risks must be explained.

## 14. Application architecture

### 14.1 Static-first PWA

The target architecture is a static-first PWA. After first installation, the complete deterministic workflow operates offline, including:

- guided intake;
- jurisdiction rules;
- protected templates;
- deterministic drafting;
- PDF creation;
- `.ics` calendar export;
- encryption and local case storage; and
- previously cached source metadata and guidance.

Opening official sources and invoking a hosted AI provider require connectivity.

The final implementation stack is not predetermined. A documented technical spike selects it using evidence.

### 14.2 Network boundary

The deterministic workflow makes no background network requests. External access uses a strict, documented allowlist and explicit user action.

Permitted categories are:

- navigation to verified official source or filing URLs;
- deliberate download of the optional browser model; and
- a deliberate call to an enabled hosted AI provider using the user’s key.

### 14.3 Hosting

Holy Cow Studios has an existing Hostinger plan and can provide a subdomain at no incremental cost. Static hosting alternatives may still be benchmarked for PWA compatibility, headers, preview deployments, free-tier constraints, geographic performance, and portability.

The final host and subdomain are selected after the technical spike. The cost constraint is zero incremental spend, not the absence of pre-existing company infrastructure.

## 15. AI architecture

### 15.1 Deterministic fallback

Every public workflow must remain fully usable without AI.

### 15.2 Local browser model

Local AI is optimized for typical laptops and desktops. Mobile and unsupported devices use the deterministic workflow.

The model:

- downloads only after explicit request;
- has a target download size of 500 MB or less;
- displays its size, licence, hardware guidance, and privacy behavior before download;
- is cached locally for reuse;
- can be removed by the user; and
- must pass the complete critical-error evaluation before being publicly enabled.

If no model within the target limit passes, local AI does not ship in the public beta.

### 15.3 Hosted bring-your-own-key adapter

The AI interface is provider-neutral with one initial provider chosen through a documented benchmark. The benchmark covers:

- English and Hindi extraction accuracy;
- structured-output/schema validity;
- critical-error rate;
- latency;
- privacy and browser security constraints;
- provider/version pinning; and
- zero-incremental-cost usability for the project.

API keys:

- remain in browser memory for the session;
- are never stored;
- are never logged;
- are never exported;
- are cleared when disconnected or the session ends; and
- are sent only to the explicitly selected, allowlisted provider.

### 15.4 AI authority limits

AI may:

- extract user-provided facts;
- normalize OCR text;
- suggest non-binding classifications; and
- highlight uncertainty.

AI may not determine or override:

- jurisdiction rules;
- fees;
- deadlines;
- filing routes;
- portal requirements;
- PIO or FAA details;
- authority addresses;
- protected legal clauses;
- mandatory warnings; or
- whether the user should appeal.

When AI and deterministic rules disagree, deterministic rules always win.

### 15.5 Version control

Exact model, provider configuration, prompt, quantization, extraction schema, and adapter version are pinned. Any change requires the full evaluation suite before release. Provider aliases that can silently change behavior cannot be treated as reproducible approved versions.

## 16. Evaluation program

### 16.1 Dataset

The initial public benchmark contains 20–30 or more synthetic grievance scenarios distributed across all five jurisdictions and major workflow branches. Expected results require expert review.

Future real cases may be added only when:

- explicit consent permits public release;
- rigorous anonymization is completed;
- provenance is recorded; and
- the designated reviewer approves publication.

The dataset, expected structured outputs, grading logic, results, and limitations are public and reproducible.

### 16.2 Primary metric

The primary metric is safety-weighted field accuracy. Critical errors receive substantially greater weight than ordinary extraction mistakes.

Critical error categories include:

- wrong jurisdiction;
- wrong fee or exemption;
- wrong deadline or date basis;
- wrong filing route;
- invented or wrong authority, PIO, FAA, or address;
- missing mandatory DPDP/officer-information caveat;
- unsupported legal assertion;
- use of stale or unapproved rule data without the required warning; and
- AI override of deterministic rules.

### 16.3 Release threshold

The public release suite must contain zero critical legal errors. A single critical failure blocks release.

An AI model or provider that fails any critical case is not offered in production. Its results may be published for research transparency.

### 16.4 Additional reported measures

Even though the primary score is safety-weighted field accuracy, reports should separately expose:

- schema validity;
- ordinary-field accuracy;
- critical-error count;
- English/Hindi consistency;
- OCR quality by document type;
- latency;
- download size and memory use for local AI;
- deterministic fallback success; and
- reviewer-rated usefulness where available.

## 17. Accessibility and browser support

The public beta targets WCAG 2.2 AA.

Required coverage includes:

- keyboard navigation;
- screen-reader semantics;
- text scaling;
- contrast;
- visible focus;
- accessible form validation and error summaries;
- reduced-motion support;
- plain-language notices; and
- accessible English and Hindi content.

Officially supported current browsers:

- Chrome;
- Edge;
- Firefox; and
- Safari.

The deterministic workflow is supported across desktop and mobile where browser primitives permit it. OCR, local AI, encryption, and PWA features use capability detection and graceful fallback.

Testing combines:

- automated Playwright tests across browser engines;
- manual testing on real Holy Cow Studios devices; and
- structured community compatibility reports.

Hindi protected templates require approval from both a proficient Hindi reviewer and the legal/RTI reviewer.

## 18. Security and privacy

### 18.1 Data minimization

The public beta has:

- no accounts;
- no analytics;
- no tracking cookies;
- no server-side case database;
- no server document upload;
- no automatic AI trace retention;
- no automatic crash reporting; and
- no email reminder service.

### 18.2 Security release baseline

Releases require:

- dependency auditing;
- secret scanning;
- static analysis;
- content-security-policy validation;
- hostile/malformed upload tests;
- file type, size, and page-count validation;
- review of cryptography and browser storage usage;
- injection and unsafe-rendering tests;
- privacy-boundary regression tests; and
- verification that diagnostic exports exclude sensitive content.

### 18.3 Diagnostic export

Technical errors may be reported through a locally generated diagnostic text/JSON file. Before export, the user previews it. It may contain:

- application and legal-data versions;
- browser capability summary;
- error category;
- non-sensitive stack/location information; and
- enabled feature flags.

It must exclude:

- case facts and grievance text;
- applicant identity and address;
- uploaded documents;
- API keys;
- passphrases and encryption material;
- AI prompts and outputs; and
- stable device identifiers.

## 19. User-facing design

The visual direction is a modern AI product: polished, distinctive, and technically credible. It must not imitate an official government site or create government-affiliation confusion.

AI is presented as an optional assistant. Reliability, privacy, and source-backed drafting lead the product messaging.

A concise not-legal-advice and independence notice appears during onboarding. Acknowledgement is required before final export. Context-specific warnings appear only where relevant to limit warning fatigue.

## 20. Feedback and community

The application links to structured GitHub issue templates for:

- software bugs;
- legal-data errors;
- accessibility issues;
- browser/device compatibility;
- security guidance; and
- feature requests.

Every public reporting surface warns users not to include personal case information.

The repository uses:

- Apache License 2.0;
- Developer Certificate of Origin sign-off;
- pull-request reviews;
- required tests;
- source citations for legal-data changes;
- Code of Conduct;
- contribution guide; and
- private security-reporting guidance.

External contributors retain copyright in their contributions and license them under Apache-2.0 unless a future, separately reviewed policy changes this arrangement.

## 21. Repository structure

The project uses one public monorepo. The exact toolchain and folder names are confirmed after the spike, but the repository must accommodate:

```text
sunwai-saathi/
├── apps/ or src/                 # PWA
├── packages/
│   ├── rules/                    # Deterministic jurisdiction engine
│   ├── templates/                # Reviewed English/Hindi templates
│   ├── documents/                # PDF and submission-pack generation
│   ├── extraction/               # OCR and AI adapters
│   └── evaluation/               # Benchmark runner and graders
├── data/
│   ├── jurisdictions/
│   ├── authorities/
│   └── sources/
├── evals/
│   ├── cases/
│   ├── expected/
│   └── reports/
├── docs/
│   ├── architecture/
│   ├── adr/
│   ├── legal-data-methodology/
│   ├── threat-model/
│   └── accessibility/
├── tests/
├── SPEC.md
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
├── LICENSE
└── NOTICE
```

## 22. Documentation requirements

The public beta requires:

- portfolio-grade README;
- product specification;
- architecture overview;
- Architecture Decision Records;
- threat model;
- privacy notice;
- legal-data methodology;
- jurisdiction support matrix;
- legal and model evaluation report;
- model card for every enabled model/provider configuration;
- accessibility statement;
- contribution guide;
- security policy;
- DCO instructions;
- deployment guide;
- user filing guide;
- supported/unsupported case guide;
- changelog; and
- known-limitations register.

## 23. Versioning and releases

Application and legal data use separate versions.

- Application: semantic versioning, for example `v1.2.0`.
- Legal dataset: independent date-oriented semantic identifier, for example `2026.08.1`.

Every submission pack and evaluation report records both.

Production releases require:

1. protected pull request checks;
2. preview deployment;
3. required technical and legal approvals where applicable;
4. passing security, accessibility, browser, and evaluation gates;
5. tagged release;
6. generated changelog; and
7. deliberate production promotion.

Merging to the main branch must not automatically publish to production.

## 24. Technical spike

The implementation stack is chosen only after a risk-focused spike demonstrates:

- installable static PWA behavior;
- full deterministic offline workflow;
- safe update behavior for versioned legal data;
- English and Hindi PDF rendering with embedded fonts;
- local PDF/image parsing and OCR;
- user-confirmed redaction preview;
- structured extraction and schema validation;
- passphrase-derived encryption and local storage;
- `.ics` calendar export;
- browser-model feasibility at or below the target size;
- provider-neutral BYOK feasibility;
- strict CSP/network allowlisting;
- acceptable initial and cached bundle sizes;
- WCAG 2.2 AA feasibility; and
- Chrome, Edge, Firefox, and Safari fallback behavior.

The spike compares candidate stacks and libraries using reproducible fixtures and records decisions in ADRs.

## 25. Milestones and gates

### Milestone 1 — Legal-data verification and product specification

Deliverables:

- this consolidated specification;
- primary-source inventory for all five jurisdictions;
- verified legal constants and change history;
- proposed legal-data schema;
- authority-selection evidence and fallback scoring;
- supported-case matrix;
- legal-review checklist;
- risk register; and
- acceptance criteria.

Gate: Akash approves the specification and verified source inventory; unreviewed legal claims are clearly separated from approved data.

### Milestone 2 — Technical feasibility spike

Deliverables:

- reproducible experiments;
- stack and library scorecard;
- bundle/performance measurements;
- OCR and Hindi PDF results;
- local-model feasibility decision;
- hosting comparison, including existing Hostinger capability;
- ADRs; and
- initial threat model.

Gate: every critical browser/privacy/document risk has a viable implementation or an accepted deterministic fallback.

### Milestone 3 — Deterministic drafting core

Deliverables:

- jurisdiction schema and validator;
- source provenance tooling;
- rules engine;
- English/Hindi protected templates;
- focused RTI draft composer;
- version stamping; and
- unit/property tests.

Gate: zero critical errors in deterministic fixtures; required reviewer approvals recorded.

### Milestone 4 — Citizen PWA workflow

Deliverables:

- onboarding and eligibility confirmation;
- guided intake;
- jurisdiction resolution;
- structured editing;
- local document handling;
- submission-pack generation;
- `.ics` export;
- optional encrypted local save; and
- accessible responsive UI.

Gate: automated acceptance suite and internal Holy Cow Studios manual scenarios pass.

### Milestone 5 — First appeal

Deliverables:

- six supported outcome categories;
- locally processed PIO-response upload;
- reviewed modular appeal grounds;
- FAA lookup behavior; and
- appeal submission pack.

Gate: zero critical errors across all first-appeal evaluation branches.

### Milestone 6 — AI assistance and evaluations

Deliverables:

- provider-neutral adapter;
- provider benchmark;
- optional approved BYOK integration;
- local-model benchmark and ship/no-ship decision;
- public synthetic benchmark;
- safety-weighted grader; and
- published reports/model cards.

Gate: no production model/provider has any critical error in the release suite.

### Milestone 7 — Public beta release

Deliverables:

- five reviewed jurisdiction profiles;
- 5–10 sourced authorities per jurisdiction;
- complete documentation set;
- accessibility and security results;
- production deployment on an approved zero-incremental-cost host/subdomain;
- tagged release and changelog; and
- GitHub feedback workflows.

Gate: all release criteria in Section 26 pass and Akash approves production promotion.

## 26. MVP completion criteria

The MVP is complete only when:

- all five jurisdiction profiles have current primary-source provenance;
- supported authority entries meet the published selection and verification standard;
- default RTI drafts request the focused record bundle;
- officer-information wording is separate, opt-in, and reviewed;
- English and Hindi templates have required approvals;
- the standard 30-day calculator labels its event basis and confidence honestly;
- all six first-appeal outcome categories work through reviewed modules;
- PDF, JPG, and PNG intake remains local;
- submission packs contain correct portal text, PDF, guidance, versions, and calendar output;
- the deterministic workflow works offline after installation;
- no account, analytics, or server case storage exists;
- optional local saves use reviewed passphrase-derived encryption;
- the public evaluation benchmark reports zero critical legal errors;
- enabled AI configurations pass the full critical suite;
- WCAG 2.2 AA checks and focused manual accessibility tests pass;
- supported-browser automation, internal acceptance tests, and documented manual checks pass;
- the security baseline passes;
- the full documentation set exists;
- technical/legal approvals are recorded where required; and
- production is deliberately promoted through the protected release workflow.

## 27. Internal acceptance testing

Initial beta usability testing is internal rather than external. Acceptance combines automated CI scenarios with manual testing by Akash and Holy Cow Studios team members.

Manual roles should cover:

- first-time citizen;
- NGO volunteer;
- English user;
- Hindi user;
- mobile user;
- desktop user;
- keyboard-only user;
- screen-reader user where internal capability permits;
- low-connectivity/offline user;
- BPL applicant scenario;
- unsupported/exceptional case; and
- first-appeal scenarios across all six outcomes.

External citizen and NGO usability research remains a recommended post-beta activity, not an MVP gate.

## 28. Risks and mitigations

| Risk | Required mitigation |
|---|---|
| Legal amendment or litigation changes interpretation | Versioned primary sources, six-month freshness warning, monthly checks, dual review, expedited hotfix |
| Wrong state fee or payment mode causes rejection | Deterministic jurisdiction profiles; zero AI authority; critical release test |
| Central/Delhi jurisdiction confusion | Independent profiles, explicit resolution, critical evaluation cases |
| Invented or stale authority/FAA address | Curated directory; designations not names; no filing-ready output without verified address |
| AI silently changes legal content | Protected templates and deterministic override |
| User mistakes RTI for grievance resolution | Records-focused language and honest onboarding |
| Sensitive document exposure | Local processing, no upload backend, explicit redaction preview, CSP allowlist |
| Shared-device case exposure | Optional passphrase encryption, local-only storage, delete control, shared-device warning |
| Browser incompatibility | Capability detection, deterministic fallback, Playwright plus manual/community testing |
| Local model too large or inaccurate | 500 MB target and no public release unless every critical case passes |
| Free service quota or vendor change | Static core, existing Hostinger option, portable deployment, deterministic offline operation |
| Government source link rot or silent replacement | Metadata, checksums, short excerpts, monthly health checks |
| Misleading AI partnership attribution | Credit Codex as an AI-assisted engineering tool, not an owner or maintainer |
| Internal-only usability blind spots | Document as known limitation; recommend post-beta external research |

## 29. Product decision governance

This specification is the frozen MVP baseline.

- Akash reviews and approves every formal milestone.
- Routine implementation decisions may be made autonomously when they remain within this specification.
- Material decisions affecting scope, legal safety, privacy, cost, architecture, or public commitments require Akash’s approval.
- Architecture changes justified by the technical spike must be recorded in ADRs.
- Superseded decisions must be removed from active requirements or explicitly marked as superseded.

Current superseded decisions:

- Email reminders and associated metadata retention were replaced by downloadable calendar reminders.
- A predetermined TypeScript stack was replaced by evidence-based selection after the technical spike.
- A generic free-host subdomain assumption was replaced by a hosting benchmark that includes Holy Cow Studios’ existing Hostinger plan and free subdomain.

## 30. Immediate next work

1. Assemble the primary-source inventory for Central, Delhi, Haryana, Maharashtra, and Goa.
2. Verify every statutory constant and jurisdiction-specific filing rule.
3. Define the legal-data and authority-directory schemas.
4. Produce the supported/unsupported scenario matrix.
5. Create the authority-selection evidence rubric and initial candidate list.
6. Draft the legal/RTI reviewer checklist.
7. Create the Milestone 1 risk register and traceability matrix.
8. Submit Milestone 1 evidence to Akash for approval before beginning the technical spike.

