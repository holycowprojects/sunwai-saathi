# Goa Research Baseline

**Dataset version:** `2026.08.5`

**Technical review date:** 27 August 2026

**Product status:** Research; not filing-ready until legal/RTI and authority review

## Technically verified behavior

| Behavior | Research value | Primary basis |
|---|---|---|
| Application fee | ₹10 | Goa RTI Fee and Cost Rules, 2006, Rule 3(1) |
| BPL treatment | No application fee; current portal requires the appropriate-government BPL certificate | RTI Act Section 7(5) and Goa portal FAQ |
| Offline payment | Cash against receipt, ₹10 court-fee stamp, demand draft, or banker's cheque payable to the concerned PIO | 2006 Rule 3(1), as amended in 2007 |
| Online payment | Internet banking, debit/credit card, or UPI through e-Challan | Current Goa portal and applicant manual |
| Application format | No exclusive prescribed application form identified in the Goa fee rules | 2006–2008 rule chain and current portal |
| Request length | Portal text field is limited to 3,000 characters; longer text may be attached as PDF | Current Goa portal FAQ |
| Portal attachment | PDF is supported; no current primary source reviewed here states a maximum application-attachment size | Current Goa portal FAQ |
| Identity evidence | No general identity-document requirement identified; BPL proof applies only to an exemption claim | Current rule chain and portal instructions |
| First-appeal fee | ₹0 | Current Goa portal FAQ |
| Online first appeal | Requires the original application registration number and email address | Current Goa portal FAQ |

## Higher-fee exception

The 2008 amendment inserted Rule 4. When rules under another applicable law prescribe a higher fee for inspection, document search, certified copies, or certified extracts, that higher fee may apply instead of the ordinary RTI information charge.

SunwaiSaathi must therefore:

1. show ₹10 as the standard application fee;
2. avoid promising that every later copy or inspection charge will use the ordinary RTI rate;
3. label an authority's additional-fee notice as requiring user review; and
4. preserve the right to challenge an excessive or incorrectly applied fee in the first-appeal workflow.

## Source conflict and uncertainty

The current portal FAQ attributes the BPL exemption to “RTI Rules, 2012,” while the official Goa law compilation and Gazettes establish the Goa-specific 2006 rules with 2007 and 2008 amendments. The FAQ may be borrowing Central-rule language, but the project will not assume why. Legal/RTI review must reconcile that reference before filing-ready activation.

The current portal advertises second-appeal filing. Second-appeal drafting remains outside SunwaiSaathi v1 scope and is not encoded as a supported product workflow.

## Review gates

1. Obtain legal/RTI approval for the consolidated 2006–2008 rules and current portal interpretation.
2. Resolve the portal FAQ's reference to “RTI Rules, 2012.”
3. Verify whether the portal applies a current attachment-size limit through an official instruction or controlled live-form test.
4. Confirm offline first-appeal form, evidence and submission requirements.
5. Select 5–10 authorities and verify designation-based PIO/FAA sources.
6. Add tests for ₹10, BPL proof, payment methods, the 3,000-character field, unknown attachment-size handling, zero first-appeal fee, and the higher-fee warning.

Until these gates pass, the Goa structured profile remains `research` and cannot produce output labelled filing-ready.
