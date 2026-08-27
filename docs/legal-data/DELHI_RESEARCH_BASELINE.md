# Government of NCT of Delhi Research Baseline

**Dataset version:** `2026.08.3`

**Technical review date:** 27 August 2026

**Product status:** Research; not filing-ready until legal/RTI approval

## Jurisdiction boundary

Government of NCT of Delhi is an independent SunwaiSaathi jurisdiction. Delhi requests must use the dedicated GNCT Delhi portal or the relevant Delhi public authority's offline route. They must never be sent through the Central RTI Online portal, which expressly excludes Government of NCT Delhi.

The Delhi portal likewise warns that it does not accept Central Government or other State Government requests and that a misfiled request may be returned without refund.

## Technically verified behavior

| Behavior | Research value | Primary basis |
|---|---|---|
| Application fee | ₹10 | Central RTI Rules, 2012 as applicable to a Union Territory administration under RTI Act Section 2(a), corroborated by the current GNCT Delhi portal manual and current department guidance |
| BPL treatment | No application or information fee; upload a certificate issued by the appropriate government | Central RTI Rules, Rule 5 and Delhi portal FAQ |
| Offline payment modes | Cash against receipt, demand draft, banker's cheque, Indian Postal Order, or available electronic means | Central RTI Rules, Rule 6 |
| Online payment | Net banking | GNCT Delhi portal and FAQ |
| Statutory application form | None identified; plain-paper filing is accepted and published forms are guidance only | Current District South East GNCT Delhi RTI page |
| Portal request field | 3,000 characters | GNCT Delhi portal FAQ; the manual's inconsistent “words” label is not used |
| Portal attachment | PDF, maximum 1 MB | GNCT Delhi portal manual |
| First-appeal fee | ₹0 | GNCT Delhi portal FAQ |
| Online first-appeal timing | Portal permits filing after 30 days from request filing or after department disposal | GNCT Delhi portal manual; statutory receipt-based logic remains controlled by RTI Act Section 19(1) |
| General identity evidence | None encoded; BPL certificate only when exemption is claimed | Portal application evidence reviewed so far |

## Legacy-material quarantine

Several current GNCT Delhi websites still publish the Delhi Right to Information Act and Rules, 2001, including historical ₹25 application and ₹50 appeal values. Other current pages mix the 2001 and 2005 workflows or link to the wrong Central portal.

SunwaiSaathi must therefore:

1. tag every 2001 Act/rules source as legacy and conflicting;
2. never import its fees, forms, authorities, deadlines, or appeal route into the RTI Act, 2005 workflow;
3. use the dedicated GNCT Delhi portal for online routing;
4. keep Delhi non-filing-ready until a legal/RTI reviewer confirms the rule-applicability analysis; and
5. prefer a current authority-specific PIO/FAA publication over personal officer names or historical directories.

## Source conflicts recorded

- The Administrative Reforms Department still publishes the 2001 Act and rules without a clear archival banner.
- A current Development Department page displays a ₹10 RTI Act, 2005 instruction alongside a historical ₹50 Delhi-Act procedure.
- A current District South East page correctly says its forms are non-statutory and plain paper is accepted, but links users to the Central portal even though both the Central and Delhi portals say GNCT Delhi requests belong on the Delhi portal.
- The portal FAQ describes a 3,000-character field, while a screenshot label in the manual says “words”. The product uses the stricter and semantically explicit 3,000-character FAQ limit.

## Review gates

1. Obtain legal/RTI approval that the Central RTI Rules, 2012 supply the applicable fee rules for GNCT Delhi authorities under the national Act.
2. Obtain a clear official archival/repeal/supersession statement for the Delhi 2001 regime, or document the controlling legal analysis.
3. Verify the live portal's covered-authority list and current payment flow.
4. Select and verify 5–10 Delhi authorities with designation-based PIO/FAA records.
5. Add tests that reject Central-portal routing, ₹25/₹50 legacy values, and the manual's misleading word-limit label.

Until these gates pass, the Delhi structured profile remains `research` and cannot produce output labelled filing-ready.
