# Primary-Source Inventory

**Status:** Research in progress; not yet legal/RTI reviewed  
**Inventory version:** 0.1.0  
**Retrieved:** 27 August 2026  
**Policy:** Only primary official sources may activate product behavior.

## Status vocabulary

| Status | Meaning | May control filing-ready output? |
|---|---|---|
| `unverified` | Located but not checked against the operative instrument | No |
| `verified` | Text, authority, scope, and effective date checked by a technical reviewer | Only after required legal/RTI approval |
| `corrected` | Earlier project claim was inaccurate and has a documented correction | Only the corrected reviewed value |
| `disputed` | Official sources or interpretations conflict | No |
| `unsupported` | Adequate primary evidence was not found | No |
| `superseded` | Replaced or repealed material retained only for history | No |

## Conflict-handling rule

When official sources conflict, appear stale, or mix repealed and current regimes:

1. do not guess which value applies;
2. record every conflicting source and its publication/effective date;
3. prefer the Gazette or current India Code text for legislation, then current rules, then the responsible official portal for operational behavior;
4. obtain legal/RTI review where applicability or interpretation remains unclear; and
5. keep the affected value or jurisdiction non-filing-ready until resolved.

## National statutory baseline

| ID | Claim/source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `IN-RTI-ACT-CURRENT` | Current RTI Act text | [India Code — consolidated Right to Information Act, 2005](https://www.indiacode.nic.in/bitstream/123456789/2065/1/aA2005-22.pdf) | Sections 6, 7, 8, 10 and 19 technically verified against the current indexed text; Section 8(1)(j) footnote gives 13 Nov 2025 effective date | `verified` (technical) | Capture checksum when India Code host is available; legal/RTI review |
| `IN-DPDP-COMMENCE-2025` | Commencement of DPDP Section 44(3) | [MeitY Gazette notification G.S.R. 843(E)](https://www.meity.gov.in/static/uploads/2025/11/c56ceae6c383460ca69577428d36828b.pdf) | Notification dated 13 Nov 2025 brings Section 44(3) into force on Gazette publication | `verified` (technical) | Legal/RTI review; SHA-256 recorded in structured source data |
| `CENTRAL-RTI-RULES-2012` | Central fee and procedure rules | [DoPT — Right to Information Rules, 2012](https://dopt.gov.in/sites/default/files/4-9-2018-IR%20Corres.PDF) | Rules 3–6 verify ₹10 fee, ordinary 500-word limit, BPL exemption/proof, information charges and payment modes | `verified` (technical) | Legal/RTI review; SHA-256 recorded in structured source data |
| `IN-DOPT-RTI-HUB` | Official legislation/rules discovery | [DoPT RTI portal](https://rti.dopt.gov.in/index.html) | Links amended Act, rules, guides, CAPIOs and state portals | `verified` (discovery) | Record exact linked files and checksums |

### Corrections already established

- The operative commencement date for DPDP Act Section 44(3) is **13 November 2025**, the notification’s Gazette publication date. The project must not encode 14 November 2025 merely because other MeitY materials were published then.
- The amended Section 8(1)(j) must be read with the rest of the current RTI Act, including Section 8(2). The product must not claim that all public-interest override analysis disappeared.
- Whether a public servant’s official-capacity identity is exempt cannot be reduced to an automatic yes/no product rule without reviewed authority. The optional clause therefore remains cautious and non-determinative.

## Central Government profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `CENTRAL-PORTAL-HOME` | Portal scope | [Central RTI Online](https://www.rtionline.gov.in/index.php) | Central authorities only; explicitly excludes state authorities and GNCT Delhi; misfiled requests may be returned without refund | `verified` (technical) | Capture reviewed date and portal snapshot metadata |
| `CENTRAL-PORTAL-GUIDE` | Online application behavior | [Central portal guidelines](https://rtionline.gov.in/guidelines.php?appeal=&pageid=45c48cce2e2d7fbdea1afc51c7c6ad26) | 3,000-character field; PDF supporting document; warns against Aadhaar/PAN except BPL proof; online payment; no first-appeal fee | `verified` (technical) | Verify file-size limit against current user manual and live form |
| `CENTRAL-PORTAL-MANUAL` | Attachment and appeal constraints | [Citizen user manual](https://rtionline.gov.in/viewPDF.php?file=um_citizen.pdf) | Indexed manual reports PDF supporting documents up to 1 MB and a 3,000-character first-appeal field; older screenshots may differ | `verified` (technical) | Hash manual; live form wins if an old screenshot conflicts |
| `CENTRAL-CPGRAMS-AUG-2025` | Candidate grievance-volume evidence | [DARPG CPGRAMS report, August 2025](https://darpg.gov.in/sites/default/files/DARPG_Monthly_Report_Central_August_2025_v6.pdf) | Ranks the ten Central ministries/departments with the highest grievance receipts from January through August 2025 | `verified` (technical) | Candidate discovery only; map domains to exact public authorities |
| `CENTRAL-CPIO-DIRECTORY` | CPIO discovery | [Central RTI Online CPIO query](https://rtionline.gov.in/request/cpioDetails_rticorner.php) | Ministry/department/public-authority lookup; the respective authorities maintain their RTI-MIS data | `verified` (discovery) | Verify each candidate's designation, service address and FAA separately |
| `CENTRAL-CIC-ANNUAL-REPORTS` | Authority-level RTI-statistics discovery | [CIC annual reports index](https://cic.gov.in/circular-reports-conventions) | Lists current and historical Section 25 annual reports | `verified` (discovery) | Extract candidate-level returns without bypassing the safe download limit |

**Profile state:** `research`; not filing-ready until the legal/RTI review, current authority directory and remaining source-capture checks pass. See [National statutory baseline](./NATIONAL_STATUTORY_BASELINE.md) and `data/jurisdictions/central.json`.

## Government of NCT of Delhi profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `DELHI-PORTAL-HOME` | Portal scope | [GNCT Delhi RTI Online](https://rtionline.delhi.gov.in/) | GNCT Delhi authorities only; excludes Central and other state authorities; supports applications and first appeals | `verified` (technical) | Verify payment modes and covered authority list |
| `DELHI-PORTAL-FAQ` | Fee, field and appeal behavior | [GNCT Delhi portal FAQ](https://rtionline.delhi.gov.in/FAQ-RTI-DL-Eng.pdf) | 3,000-character request field, PDF attachment, BPL proof, Net banking and no first-appeal fee | `verified` (technical) | Legal/RTI review; hash recorded in structured source data |
| `DELHI-PORTAL-MANUAL` | Portal workflow | [GNCT Delhi citizen manual](https://rtionline.delhi.gov.in/UMcitizen_Eng.pdf) | Shows ₹10 fee, PDF attachment up to 1 MB and first appeal after 30 days or disposal; screenshot word-limit label conflicts with FAQ | `verified` (technical) | Use stricter FAQ character limit; legal/RTI review; hash recorded |
| `DELHI-LEGACY-2001` | Legacy-law warning | [Delhi Administrative Reforms — Delhi RTI Rules 2001](https://ard.delhi.gov.in/rti/right-information-rules-2001) | Official site still publishes the 2001 regime and historical ₹25/₹50 values without a clear archival banner | `disputed` | Quarantine from 2005 Act workflow; document controlling applicability/supersession analysis |
| `DELHI-FORMS-GUIDANCE` | Non-statutory forms | [District Magistrate South East RTI page](https://dmsoutheast.delhi.gov.in/rti/) | Forms are guidance and plain paper is accepted, but its Central-portal link conflicts with both portals' scope warnings | `verified` (technical, form status only) | Use Delhi portal for routing; confirm plain-paper position across GNCT authorities |

**Profile state:** `research`; legacy Delhi material is quarantined and the profile is non-filing-ready pending legal/RTI approval, authority coverage verification and resolution of official-site conflicts. See [Delhi research baseline](./DELHI_RESEARCH_BASELINE.md).

## Haryana profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `HARYANA-RTI-RULES-2009` | Base state rules | [Chief Secretary Office — Haryana RTI Rules, 2009](https://csharyana.gov.in/WriteReadData/Notifications%20%26%20Orders/Administrative%20Reforms/3813.pdf) | Effective 1 Jan 2010; preferred Model Form A, payment procedure and manual second-appeal process | `verified` (technical) | Legal/RTI review with all amendments; hash recorded |
| `HARYANA-RTI-AMEND-2016` | Fee and length amendment | [Haryana Gazette — 2016 amendment](https://csharyana.gov.in/WriteReadData/Notifications%20%26%20Orders/Administrative%20Reforms/5380.pdf) | Substituted Rule 5: ₹10 application fee, ordinary 500-word limit and no rejection solely for excess length | `verified` (technical) | Legal/RTI review; hash recorded |
| `HARYANA-RTI-AMEND-2021` | Identity-form amendment | [Haryana Gazette — 2021 amendment](https://csharyana.gov.in/WriteReadData/Rules/Administrative%20Reforms/11941.pdf) | Replacement Model Form A requires one of six categories of government identity evidence | `verified` (technical) | Legal/RTI and privacy review; hash recorded |
| `HARYANA-RTI-IDENTITY-2024` | Identity enforcement | [20 May 2024 compliance circular](https://csharyana.gov.in/WriteReadData/Circular-%26-Instructions/Administrative-Reforms/14492.pdf) | Directs Haryana authorities to comply with the 2021 identity-proof requirement | `verified` (technical) | Legal/RTI and privacy review; hash recorded |
| `HARYANA-PORTAL-HOME` | Portal scope/payment | [Haryana RTI portal](https://rtiharyana.gov.in/) | Haryana authorities only; lists Net Banking, cards, UPI, NEFT, RTGS and e-Challan; reports desktop-oriented and headquarters-routing limitations | `verified` (technical) | Verify live authority list and payment behavior |
| `HARYANA-PORTAL-MANUAL` | Request and first-appeal operation | [Haryana citizen manual](https://rtiharyana.gov.in/pdffiles/UserManualforCitizen.pdf) | Subject 1,000 characters; description 5,000; PDF up to 20 MB; no first-appeal fee; lists appeal evidence | `verified` (technical) | Legal/RTI review; hash recorded |

**Profile state:** `research`; operative rule chain and portal behavior are technically captured, including the identity-proof requirement, but filing-ready output remains blocked pending legal/RTI, privacy and authority review. See [Haryana research baseline](./HARYANA_RESEARCH_BASELINE.md).

## Maharashtra profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `MH-RTI-RULES-2005` | Legacy base rules | [Maharashtra State Information Commission copy of the 2005 Rules](https://sic.maharashtra.gov.in/site/Downloads/GR/11.10.2005%20%E0%A4%AE%E0%A4%BE%E0%A4%B9%E0%A4%BF%E0%A4%A4%E0%A5%80%E0%A4%9A%E0%A4%BE%20%E0%A4%85%E0%A4%A7%E0%A4%BF%E0%A4%95%E0%A4%BE%E0%A4%B0%20%E0%A4%85%E0%A4%A7%E0%A4%BF%E0%A4%A8%E0%A4%BF%E0%A4%AF%E0%A4%AE%202005%20%E0%A4%AC%E0%A4%BE%E0%A4%AC%E0%A4%A4.pdf) | Notification dated 11 Oct 2005; Rule 3 prescribes Annexure A and a ₹10 application fee payable by cash receipt, demand draft, banker's cheque, or ₹10 court-fee stamp | `verified` (technical) | Legal/RTI review and Gazette cross-check |
| `MH-RTI-AMEND-2012-SINGLE-SUBJECT` | Legacy application constraint | [Maharashtra RTI circular index and official notification download](https://rti.maharashtra.gov.in/circular) | Notification dated 16 Jan 2012 inserts Rule 3A: one subject per request, ordinarily no more than 150 words; separate applications for additional subjects | `verified` (technical) | Legal/RTI review and Gazette cross-check |
| `MH-RTI-SECOND-AMEND-2012-INSPECTION` | Record-inspection procedure | [Official MSEDCL compilation](https://elibrary.mahadiscom.in/data/hrl/oebooks/AdmCircular-II.pdf) | Gazette notification dated 31 Jan 2012 inserts Rule 3B: supervised inspection during office hours, pencil only and no marking | `verified` (technical) | Legal/RTI review; hash recorded |
| `MH-RTI-NOTIFICATION-2013-FEE-FORM` | Payment and information-fee amendment | [Maharashtra RTI circular index and official notification download](https://rti.maharashtra.gov.in/circular) | Adds Indian Postal Order to Rules 3, 4 and 5; revises inspection timing and sample/model costs | `verified` (technical) | Independent Marathi and legal/RTI review of visual transcription; hash recorded |
| `MH-RTI-FORMAT` | Application and appeal forms/fees | [Maharashtra State Information Commission RTI format](https://sic.maharashtra.gov.in/site/Downloads/Important_Letters/RTI%20Format.pdf) | Annexure A uses a ₹10 court-fee stamp; Annexure B uses a ₹20 court-fee stamp and calls for copies of the application and PIO correspondence | `verified` (technical) | Legal/RTI review; hash recorded |
| `MH-PORTAL-FAQ` | Online first-appeal operation | [Maharashtra RTI Online FAQ](https://rtionline.maharashtra.gov.in/FAQ-RTI-Online.pdf) | Online first appeal is ₹20, uses the original registration number and routes through the public authority's nodal officer | `verified` (technical) | Legal/RTI review; hash recorded |
| `MH-PORTAL-MANUAL` | Online application and first-appeal workflow | [Maharashtra citizen manual](https://rtionline.maharashtra.gov.in/UMcitizen_Eng_maha.pdf) | 150-word request field; PDF up to 1 MB; BPL certificate; ₹10/₹20 fees; net banking and major cards | `verified` (technical) | Reconcile its “RTI Rules, 2012” references; hash recorded |
| `MH-RULES-AMEND-2026` | Current amendment | [Maharashtra RTI Amendment Rules, 2026](https://rtionline.maharashtra.gov.in/webroot/GR/RTI_Amenment_rule_2026.pdf) | Notification dated 19 Jun 2026 replaces Annexure A and includes a proof-of-identity field | `verified` (technical) | Hash PDF; locate and verify underlying 2026 rules and fee provisions |
| `MH-PORTAL-HOME` | Portal scope and authority directory | [Maharashtra RTI Online](https://rtionline.maharashtra.gov.in/) | Applications and first appeals for listed Maharashtra authorities; excludes Central and other State authorities; live page also publishes deferred 2026 material | `verified` (technical) | Use only operational behavior in v1; legal/RTI review |
| `MH-RULES-HUB` | Official rules discovery | [Maharashtra Directorate of Municipal Administration RTI page](https://mahadma.maharashtra.gov.in/en/rti/) | Links current Maharashtra RTI Rules, 2026 and official portal | `verified` (discovery) | Resolve underlying rules file URL and checksum |

**Profile state:** `v1-legacy-baseline-research`. Maharashtra remains in MVP scope and may produce filing-ready output in v1 after the pre-June-2026 baseline receives the required legal/RTI approval. The baseline includes Rule 3A's single-subject requirement and ordinary 150-word limit, introduced in 2012. The claimed ₹30 fee, mandatory photo-ID field, revised 2026 forms, and any other change introduced only by the disputed 2026 instruments must not be encoded in v1.

See [Maharashtra v1 legacy baseline](./MAHARASHTRA_V1_BASELINE.md) for the exact product policy, verified values, checksums, and remaining review gates.

### Maharashtra 2026 status conflict

- Official Maharashtra portals continue to publish and link the Maharashtra Right to Information Rules, 2026 and the 19 June 2026 amendment.
- Multiple credible news organizations reported on 2 July 2026 that the State Government placed the new rules in abeyance.
- A news report, political statement, or portal banner is not sufficient to resolve the operative legal position under the project’s primary-source-only policy.
- Required resolution evidence is a Gazette notification, government order/circular, State Information Commission order, or another primary official instrument that clearly states the rules’ current legal or operational status.
- V1 deliberately uses the pre-June-2026 rules after those rules are independently verified from primary official sources. This is a product-version policy, not a conclusion about the legal effect of the reported stay.
- Every Maharashtra v1 submission pack must identify the pre-June-2026 rules baseline and its last verification date.
- The legal and operational status of the 2026 rules is deferred to the v2 research cycle. V2 must not change Maharashtra behavior until primary official evidence and legal/RTI review are complete.

## Goa profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `GOA-RTI-RULES-CONSOLIDATED` | Consolidated state fee rules | [Goa government-hosted RTI Act and Rules compilation](https://tcp.goa.gov.in/wp-content/uploads/2016/11/rti.pdf) | ₹10 application fee; cash, court-fee stamp, demand draft or banker's cheque; information charges and 2008 higher-fee exception | `verified` (technical) | Legal/RTI review; hash recorded |
| `GOA-RTI-AMEND-2007` | Court-fee-stamp amendment | [Official Gazette Series I No. 17](https://goaprintingpress.gov.in/downloads/0708/0708-17-SI-OG.pdf) | Adds a ₹10 court-fee stamp as an application-fee method | `verified` (technical) | Legal/RTI review; hash recorded |
| `GOA-RTI-AMEND-2008` | Higher-fee exception | [Official Gazette Series I No. 46](https://goaprintingpress.gov.in/downloads/0708/0708-46-SI-OG.pdf) | Rule 4 permits higher inspection/search/certified-copy fees prescribed by rules under another applicable law | `verified` (technical) | Legal/RTI review and product-warning approval; hash recorded |
| `GOA-PORTAL-HOME` | Portal scope and filing stages | [Goa RTI Online](https://rtionline.goa.gov.in/) | Applications and first/second appeals for Goa State authorities; e-Challan supports Internet banking, cards and UPI | `verified` (technical) | Verify covered authority list; second appeal remains out of v1 scope |
| `GOA-PORTAL-FAQ` | Request and first-appeal operation | [Goa RTI Online FAQ](https://rtionline.goa.gov.in/FAQ.pdf) | 3,000-character field, PDF overflow attachment, BPL certificate, zero first-appeal fee, registration number and email required online | `verified` (technical) | Resolve unexplained “RTI Rules, 2012” reference; hash recorded |
| `GOA-PORTAL-MANUAL` | Application/payment workflow | [Goa applicant module manual](https://rtionline.goa.gov.in/Applicant_Module_User_Manual.pdf) | ₹10 fee, BPL card details, online payment, receipt, additional-payment and reply workflows | `verified` (technical) | Legal/RTI review; hash recorded |
| `GOA-LEGACY-1997` | Legacy-law warning | [Goa Department of Information — Goa RTI Act 1997](https://dip.goa.gov.in/goa-right-to-information-act-1997/) | Official site retains pre-national-Act state law | `superseded` pending legal confirmation | Must not populate current workflow; document repeal/supersession authority |

**Profile state:** `research`; the 2006–2008 rule chain and current portal behavior are technically captured, but filing-ready output remains blocked pending legal/RTI review, resolution of the portal's 2012-rules reference, attachment-limit confirmation and authority review. See [Goa research baseline](./GOA_RESEARCH_BASELINE.md).

## Checksum backlog

Checksums are intentionally pending until source files are downloaded through a reproducible source-capture script. The future script must:

1. accept only allowlisted official URLs from structured source records;
2. save files outside tracked source data by default;
3. calculate SHA-256 over raw response bytes;
4. record retrieval time, response content type, size and resolved URL;
5. require review before a changed checksum updates an approved record; and
6. never treat availability or an unchanged checksum as proof that a rule remains legally operative.
