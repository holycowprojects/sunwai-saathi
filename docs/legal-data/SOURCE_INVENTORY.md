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
| `IN-RTI-ACT-CURRENT` | Current RTI Act text | [India Code — Right to Information Act, 2005](https://www.indiacode.nic.in/handle/123456789/2065?view_type=browse) | Authoritative Act index; current PDF must be hashed and section text extracted | `unverified` | Capture current PDF checksum; verify Sections 3, 6, 7, 8, 10 and 19 |
| `IN-DPDP-COMMENCE-2025` | Commencement of DPDP Section 44(3) | [MeitY Gazette notification G.S.R. 843(E)](https://www.meity.gov.in/static/uploads/2025/11/c56ceae6c383460ca69577428d36828b.pdf) | Notification dated 13 Nov 2025 brings Section 44(3) into force on Gazette publication | `verified` (technical) | Hash PDF; legal/RTI review; record Gazette publication metadata |
| `IN-RTI-RULES-2012` | Central fee and procedure rules | [DoPT — Right to Information Rules, 2012](https://dopt.gov.in/sites/default/files/4-9-2018-IR%20Corres.PDF) | Official copy of G.S.R. 603(E), dated 31 Jul 2012 | `unverified` | Verify application fee, BPL rule, payment modes, copying/inspection charges |
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
| `CENTRAL-PORTAL-MANUAL` | Attachment and appeal constraints | [Citizen user manual](https://rtionline.gov.in/viewPDF.php?file=um_citizen.pdf) | Manual reports PDF supporting document up to 1 MB and 3,000-character first-appeal text | `unverified` | Hash manual; reconcile publication age with current live form |

**Profile state:** `unverified`; not filing-ready until fee/rules and live portal behavior receive legal/RTI review.

## Government of NCT of Delhi profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `DELHI-PORTAL-HOME` | Portal scope | [GNCT Delhi RTI Online](https://rtionline.delhi.gov.in/) | GNCT Delhi authorities only; excludes Central and other state authorities; supports applications and first appeals | `verified` (technical) | Verify payment modes and covered authority list |
| `DELHI-PORTAL-FAQ` | Appeal behavior | [GNCT Delhi portal FAQ](https://rtionline.delhi.gov.in/FAQ-RTI-DL-Eng.pdf) | Online first appeal uses original registration; FAQ says no first-appeal fee | `unverified` | Hash PDF; verify against operative Delhi rules |
| `DELHI-PORTAL-MANUAL` | Portal workflow | [GNCT Delhi citizen manual](https://rtionline.delhi.gov.in/UMcitizen_Eng.pdf) | Manual states first appeal can follow 30-day lapse or request disposal | `unverified` | Hash PDF; verify exact timing wording against Act |
| `DELHI-LEGACY-2001` | Legacy-law warning | [Delhi Administrative Reforms — Delhi RTI Rules 2001](https://ard.delhi.gov.in/rti/right-information-rules-2001) | Official site still publishes pre-national-Act Delhi law/rules | `superseded` pending legal confirmation | Must never populate 2005 Act workflow; document repeal/supersession authority |
| `DELHI-FORMS-GUIDANCE` | Non-statutory forms | [District Magistrate South East RTI page](https://dmsoutheast.delhi.gov.in/rti/) | Official page says forms are guidance and applications may be on plain paper | `unverified` | Confirm whether this generalizes across GNCT Delhi authorities |

**Profile state:** `disputed/unverified`; legacy Delhi material must be separated before activation.

## Haryana profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `HARYANA-PORTAL-HOME` | Portal scope/payment | [Haryana RTI portal](https://rtiharyana.gov.in/) | Haryana authorities only; lists Net Banking, cards, UPI, NEFT, RTGS and e-Challan; reports desktop-oriented portal limitations | `verified` (technical) | Verify live covered authority list and current payment behavior |
| `HARYANA-PORTAL-MANUAL` | First-appeal operation | [Haryana citizen manual](https://rtiharyana.gov.in/pdffiles/UserManualforCitizen.pdf) | Online first appeal, no stated fee, PDF supporting documents up to 20 MB | `unverified` | Hash document; reconcile with operative 2009 rules |
| `HARYANA-RULES-2009` | Operative state rules | Referenced by official portal as Haryana Right to Information Rules, 2009 | Portal references Rule 6 for manual second appeals | `unverified` | Locate Gazette/official rules PDF; verify all fee/form/appeal provisions |

**Profile state:** `unverified`; no fee value or filing-ready output until the operative rules are obtained.

## Maharashtra profile

| ID | Source role | Official source | Preliminary finding | Status | Follow-up |
|---|---|---|---|---|---|
| `MH-RULES-AMEND-2026` | Current amendment | [Maharashtra RTI Amendment Rules, 2026](https://rtionline.maharashtra.gov.in/webroot/GR/RTI_Amenment_rule_2026.pdf) | Notification dated 19 Jun 2026 replaces Annexure A and includes a proof-of-identity field | `verified` (technical) | Hash PDF; locate and verify underlying 2026 rules and fee provisions |
| `MH-PORTAL-HOME` | Portal scope | [Maharashtra RTI Online](https://rtionline.maharashtra.gov.in/) | Maharashtra authorities only; application and first-appeal portal | `verified` (technical) | Verify coverage, payment methods, limits and current instructions |
| `MH-RULES-HUB` | Official rules discovery | [Maharashtra Directorate of Municipal Administration RTI page](https://mahadma.maharashtra.gov.in/en/rti/) | Links current Maharashtra RTI Rules, 2026 and official portal | `verified` (discovery) | Resolve underlying rules file URL and checksum |

**Profile state:** `v1-legacy-baseline`. Maharashtra remains in MVP scope and may produce filing-ready output in v1 using only the last primary-source-verified rules that applied before the June 2026 publication. The claimed ₹30 fee, mandatory photo-ID requirement, one-subject restriction, and revised 2026 forms must not be encoded in v1.

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
| `GOA-PORTAL-HOME` | Authority directory and portal discovery | [Goa RTI citizen gateway](https://rti.goa.gov.in/) | Official department/office directory and links to state RTI services | `verified` (technical) | Map online application/first-appeal availability and coverage |
| `GOA-RULES-2006` | State fee rules | [Goa government-hosted RTI Act and Rules compilation](https://tcp.goa.gov.in/wp-content/uploads/2016/11/rti.pdf) | Compilation states ₹10 application fee via cash, ₹10 court-fee stamp, demand draft or banker’s cheque; includes 2007 amendment | `unverified` | Hash file; confirm no later amendments; legal/RTI review |
| `GOA-REQUEST-GUIDE` | General request guidance | [Goa request-information guide](https://rti.goa.gov.in/requestforinf.aspx) | Describes writing/electronic request, BPL exemption, standard timing and delayed-information fee consequence | `unverified` | Separate exceptional timing because MVP supports standard cases only |
| `GOA-LEGACY-1997` | Legacy-law warning | [Goa Department of Information — Goa RTI Act 1997](https://dip.goa.gov.in/goa-right-to-information-act-1997/) | Official site retains pre-national-Act state law | `superseded` pending legal confirmation | Must not populate current workflow; document repeal/supersession authority |

**Profile state:** `unverified`; confirm current rules/amendments and online first-appeal route.

## Checksum backlog

Checksums are intentionally pending until source files are downloaded through a reproducible source-capture script. The future script must:

1. accept only allowlisted official URLs from structured source records;
2. save files outside tracked source data by default;
3. calculate SHA-256 over raw response bytes;
4. record retrieval time, response content type, size and resolved URL;
5. require review before a changed checksum updates an approved record; and
6. never treat availability or an unchanged checksum as proof that a rule remains legally operative.
