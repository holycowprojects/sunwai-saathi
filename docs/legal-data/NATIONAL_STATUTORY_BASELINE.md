# National RTI Statutory Baseline

**Dataset version:** `2026.08.2`

**Technical review date:** 27 August 2026

**Product status:** Research; not filing-ready until legal/RTI approval

## Deterministic statutory constants

These values must be loaded from versioned legal data. They must never be recalled or rewritten by an AI model.

| Provision | Deterministic product rule |
|---|---|
| RTI Act Sections 6(1)–(2) | Accept a written or electronic request in English, Hindi, or the official language of the area; route it to the relevant CPIO/SPIO or designated assistant PIO and apply the prescribed fee rules. Under Section 6(2), the applicant does not have to give reasons for the request. |
| RTI Act Section 6(3) | A receiving public authority should transfer an application, or the relevant part, as soon as practicable and no later than five days when the information is held by, or more closely connected with, another public authority. Transfer-adjusted deadline calculation is unsupported in the MVP. |
| RTI Act Section 7(1) | For a standard supported case, the PIO must decide the request as expeditiously as possible and no later than 30 days after receipt. SunwaiSaathi must identify the receipt event used; it must not silently treat a drafting or payment date as confirmed receipt. |
| RTI Act Section 7(6) | Information must be supplied free of charge when the public authority fails to comply with the applicable Section 7(1) time limit. |
| RTI Act Section 19(1) | A first appeal may be filed within 30 days after the response period expires or within 30 days after receipt of the decision; delayed appeals may be admitted for sufficient cause. The appeal goes to an officer senior in rank to the PIO. |
| RTI Act Section 19(3) | A second appeal may be filed within 90 days after the decision should have been made or was actually received; delayed appeals may be admitted for sufficient cause. Second-appeal drafting is outside v1. |
| RTI Act Section 19(6) | A first appeal should be disposed of within 30 days after receipt, or within a total of 45 days for reasons recorded in writing. This is a statutory disposal period, not a promise that the grievance itself will be resolved. |
| RTI Act Section 8(1)(j) | From 13 November 2025, the clause reads: “information which relates to personal information”. The product must not reproduce the superseded clause. |
| RTI Act Section 8(2) | The public-interest override remains in the consolidated Act. The product must not state categorically that every possible public-interest route was removed. |

The life-or-liberty 48-hour route, APIO-added time, Section 6(3) transfers, third-party procedure, exempt organisations, and additional-fee timing are outside the MVP deadline calculator. The interface may explain them but must not produce a filing-ready deadline for them.

## Officer-information opt-in caveat — draft for expert review

> Optional request: You may ask for records that identify the official roles or officers involved in processing the file. Since Section 8(1)(j) of the RTI Act was amended with effect from 13 November 2025, information relating to an identifiable person may be refused as personal information. The application keeps this request separate so its refusal need not affect the file-noting and action-taken requests. Disclosure depends on the records, context, other provisions of the Act, and the decision of the competent authority.

This wording is deliberately non-determinative. It must remain disabled in filing-ready output until legal/RTI review approves it in both English and Hindi.

## Change history

| Effective date | Change | Product consequence |
|---|---|---|
| 12 Oct 2005 | Remaining substantive provisions of the RTI Act came into force | National request and appeal framework |
| 31 Jul 2012 | Central Right to Information Rules, 2012 came into force on Gazette publication | ₹10 fee, ordinary 500-word rule, BPL proof, payment modes and information charges |
| 13 Nov 2025 | DPDP Act Section 44(3) commenced through G.S.R. 843(E) | Replace Section 8(1)(j) text and show reviewed caveat for optional officer-information requests |

## Review gates

1. Obtain legal/RTI approval for every statutory interpretation and the officer-information caveat.
2. Capture a reproducible checksum for the current consolidated India Code RTI Act PDF; its host was unavailable during local capture on 27 August 2026.
3. Re-check the consolidated Act for later amendments before approval.
4. Approve English and Hindi protected wording separately.
5. Add boundary tests for receipt dates, 30-day and 90-day windows, the 45-day extension, and unsupported timing branches.
