# Central Government authority candidate evidence

**Status:** Candidate discovery; no scored or selected authority

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
