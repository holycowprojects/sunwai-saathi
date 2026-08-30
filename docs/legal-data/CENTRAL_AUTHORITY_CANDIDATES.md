# Central Government authority candidate evidence

**Status:** Candidate discovery and technical scoring; no verified launch authority

**Evidence date:** 30 August 2026

This dossier begins the Central Government authority-selection work. It uses official grievance volume to identify high-value candidates, then requires separate PIO, FAA, address, route and freshness verification under [the authority-selection methodology](./AUTHORITY_SELECTION.md).

## Official grievance evidence

DARPG's August 2025 CPGRAMS report provides the ten Central ministries/departments with the highest grievance receipts from 1 January through 31 August 2025.

| Rank | Ministry/department as reported | Grievance receipts | Candidate interpretation |
|---:|---|---:|---|
| 1 | Ministry of Labour and Employment | 165,560 | Strong candidate domain; the report attributes a large share of monthly grievances to EPFO, so ministry-versus-EPFO routing must be resolved before scoring |
| 2 | Department of Financial Services (Banking Division) | 118,048 | Strong candidate domain; bank-specific public-authority routing may differ from department routing |
| 3 | Department of Telecommunications | 55,014 | Strong candidate domain for telecom-service grievances |
| 4 | Ministry of Railways (Railway Board) | 50,671 | Strong candidate domain; zonal/operational authority boundaries require verification |
| 5 | Department of Posts | 45,506 | Strong candidate domain with nationwide citizen-service relevance |
| 6 | Ministry of Home Affairs | 45,232 | High volume but broad and potentially sensitive; division and exempt-organisation boundaries require careful support rules |
| 7 | Central Board of Direct Taxes (Income Tax) | 44,231 | Strong candidate domain; regional and functional authority routing requires verification |
| 8 | Department of Agriculture and Farmers Welfare | 38,027 | Strong candidate domain; scheme and implementing-authority boundaries require verification |
| 9 | Department of Health and Family Welfare | 32,576 | Strong candidate domain; attached bodies and institution-specific routing require verification |
| 10 | Unique Identification Authority of India | 28,802 | Strong candidate domain; identity-related privacy safeguards and regional routing require verification |

These counts are grievance receipts, not RTI applications, unique citizens, unresolved grievances or findings of fault. They rank candidate domains only and must not be presented as performance scores.

## Additional official discovery sources

- The Central RTI Online CPIO query provides ministry, department and public-authority discovery and says the respective public authorities maintain their CPIO data in RTI-MIS.
- The CIC annual-report index provides the Section 25 annual-return evidence path. Its current report can supplement the grievance ranking with authority-level RTI activity and reporting-compliance data.
- Neither source alone proves a complete designation-based PIO and FAA service address.

## Safety and capture decision

The CIC index's current English annual-report file resolved above the project's 10 MB safe local-download limit. It was not downloaded, opened locally, executed or committed. The official HTML index is recorded as a discovery source; any later large-file review must use a separately approved safe method or an official smaller derivative.

## Preliminary candidate pool

The ten reported domains form the initial pool, not the final launch list. No scorecard is created until evidence can distinguish the correct public authority from a ministry, scheme, attached office, regional office or public-sector entity.

For each domain, the next review must establish:

1. exact Central public-authority identity and portal label;
2. grievance-to-record relevance for the supported stuck-grievance workflow;
3. designation-based CPIO office and service address;
4. designation-based FAA office and service address;
5. verified online and offline filing routes;
6. current official directory source with a maintainable update path; and
7. authority-level RTI annual-return evidence where available.

Until those checks and the rubric score pass, every entry remains candidate discovery only and cannot populate filing-ready output.

## Candidate review 1 — Department of Posts

**Weighted research score:** `66.25/100`

**Decision:** `research`; blocked by hard gates

| Dimension | Score | Finding |
|---|---:|---|
| Population served | 4/4 | Current official structure covers postal circles across India |
| Grievance relevance | 4/4 | Fifth-highest Central grievance receipts in the official January–August 2025 table |
| Source completeness | 1/4 | No complete current designation-based CPIO/FAA and service-address mapping verified |
| Filing accessibility | 2/4 | Central mechanisms exist, but the correct circle/division/functional unit is unresolved |
| Maintainability | 1/4 | Evidence is fragmented; several previously indexed official CPIO/FAA pages returned 404 during the current review |

The Department is not one safely addressable RTI office for MVP purposes. Postal records may sit with a circle, region, division, directorate function or other unit. The current India Post RTI structure page exposes separate circle documents, while older indexed directory pages cannot be treated as current merely because search text remains available.

This candidate fails the minimum `sourceCompleteness >= 3` and `maintainability >= 2` selection gates. Its numerical score cannot override those failures. It must not produce filing-ready output or be converted to an authority record.

Required follow-up:

1. locate a current official landing page for the complete CPIO and FAA directory;
2. determine whether a stable designation-based mapping exists by grievance subject and postal geography;
3. confirm the exact Central RTI Online public-authority labels;
4. verify a service address for each supported routing unit; and
5. reassess whether supporting this authority would require a nested routing model beyond the current MVP authority schema.

## Candidate review 2 — Department of Telecommunications

**Weighted research score:** `91.25/100`

**Decision:** `selected-pending-verification`; freshness gate failed

| Dimension | Score | Finding |
|---|---:|---|
| Population served | 4/4 | National telecommunications-policy and citizen-service reach |
| Grievance relevance | 4/4 | Third-highest Central grievance receipts in the official January–August 2025 table |
| Source completeness | 3/4 | Central RTI Cell, subject-mapped CPIO/FAA designations, rooms and main address found; directory freshness remains insufficient |
| Filing accessibility | 4/4 | Central intake can forward within DoT; online and offline routes exist |
| Maintainability | 3/4 | Stable dated matrix exists, but it contains changing incumbents and needs a current designation-only refresh |

DoT's official administrative chapter says its RTI Cell receives applications and appeals for the Department and forwards them to the relevant CPIO or FAA. It also warns that attached/subordinate offices and societies are separate public authorities. SunwaiSaathi must therefore restrict this candidate to records held by DoT itself and must not silently route TRAI, BSNL, MTNL, field units or another body through the Department.

The 5 December 2025 matrix is well structured but exceeds the project's six-month freshness window on the evidence date. All substantive directory gates pass except `currentWithinReviewWindow`. The candidate cannot become `verified-launch-candidate` until a current official matrix or explicit current confirmation is found and reviewed.

Required follow-up:

1. locate a matrix dated within the active freshness window or obtain official confirmation that the December 2025 matrix remains current;
2. convert the subject mapping to designation-based records without names, phone numbers or email addresses;
3. verify the exact Central RTI Online label through a controlled portal check;
4. define the safe unsupported exit for grievances belonging to a separate public authority; and
5. obtain technical and legal/RTI directory approval.

## Candidate review 3 — Unique Identification Authority of India

**Weighted research score:** `93.75/100`

**Decision:** `selected-pending-verification`; current directory files located but not independently inspected

| Dimension | Score | Finding |
|---|---:|---|
| Population served | 4/4 | National authority with Head Office and eight Regional Offices covering all States and Union Territories |
| Grievance relevance | 4/4 | Top-ten Central grievance domain and 3,979 RTI applications handled in 2024–25 |
| Source completeness | 3/4 | Current dated Head Office and Regional Office directory files are linked, but their full designation/address contents remain uninspected |
| Filing accessibility | 4/4 | Nodal RTI Cell processes online/offline applications and appeals; regional routing is published |
| Maintainability | 4/4 | Stable maintained hub, dated current lists and archives |

Authority identity, filing-route and freshness gates pass on the evidence date. PIO designation, FAA designation and service-address gates remain false until the linked 18 May 2026 files are independently inspected. The candidate also requires legal/RTI approval, exact Central portal-label confirmation and privacy-safe routing fixtures.

### Mandatory privacy boundary

UIDAI's own RTI disclosures acknowledge that applications and appeals may contain identifiers and contact data. SunwaiSaathi must not ask for or store an Aadhaar number to select an authority or Regional Office. Routing uses the grievance's State/UT and record-owning office; any case reference needed in a draft remains local, user-confirmed and excluded from logs, diagnostics, examples and repository fixtures.

### Stale statutory text conflict

The current UIDAI RTI hub reproduces the superseded pre-13-November-2025 text of Section 8(1)(j), including the former privacy/public-interest wording. That page is valid directory evidence but disputed legal-text evidence. SunwaiSaathi must quarantine its statutory paragraph and always use the current India Code/DPDP baseline for legal wording and the officer-information caveat.

Required follow-up:

1. independently review the 18 May 2026 Head Office and Regional Office lists;
2. encode designation-based regional routing without copying incumbent names or contact details;
3. verify the exact Central RTI Online public-authority label;
4. create privacy tests proving Aadhaar numbers cannot enter routing, logs, diagnostics or fixtures;
5. add a regression test that the UIDAI page's superseded Section 8(1)(j) text can never override the national legal dataset; and
6. obtain technical and legal/RTI directory approval.

## Candidate review 4 — Employees' Provident Fund Organisation

**Weighted research score:** `71.25/100`

**Decision:** `research`; source-completeness and freshness gates failed

| Dimension | Score | Finding |
|---|---:|---|
| Population served | 4/4 | Official indexed material reports 29.88 crore member accounts and 147 offices across India |
| Grievance relevance | 4/4 | Labour and Employment leads the official Central grievance table, with EPFO identified as a major contributing organisation |
| Source completeness | 2/4 | RTI, directory and locator paths exist, but no complete current designation-based CPIO/FAA mapping was verified |
| Filing accessibility | 1/4 | Central and EPFO discovery paths exist, but the exact portal label, record-owning office and complete offline addressee remain unverified |
| Maintainability | 2/4 | A national locator exists, but it warns that its data is under field-office verification and indexed directory pages failed direct retrieval |

EPFO is a strong user-problem fit but a poor candidate for guessed routing. Member, claim, pension, employer and establishment records may be held by different field or functional offices. The official locator can help a user confirm the relevant office, but its own verification warning prevents SunwaiSaathi from treating the result as authoritative filing-ready evidence.

The indexed official RTI hub and office-directory pages appeared recently maintained, but direct retrieval returned 404 during this review. They remain disputed discovery records rather than active directory evidence. The score falls in the shortlist range, but `sourceCompleteness < 3`, failed filing-route and freshness gates, and the unresolved custody boundary keep the candidate in `research`.

### Mandatory privacy boundary

Authority routing must not ask for a UAN, Aadhaar number, claim number, employer code, password, OTP or account credential. State/UT, district, grievance subject and a user-confirmed record-owning office are sufficient for routing research. Any reference included in the final draft remains local and must be excluded from repository fixtures, analytics, logs and diagnostics.

Required follow-up:

1. locate a current official designation-based CPIO and FAA directory for Head Office and field offices;
2. verify complete service addresses and the exact Central RTI Online authority labels;
3. define deterministic subject-and-geography routing with mandatory user confirmation;
4. create a safe unsupported exit when the record-owning office cannot be established;
5. add privacy tests for UAN, Aadhaar, claim and credential fields; and
6. obtain technical and legal/RTI directory approval.
