# Haryana Research Baseline

**Dataset version:** `2026.08.4`

**Technical review date:** 27 August 2026

**Product status:** Research; not filing-ready until legal/RTI approval

## Technically verified behavior

| Behavior | Research value | Primary basis |
|---|---|---|
| Application fee | ₹10 | Rule 5 substituted by the Haryana RTI Amendment Rules, 2016 |
| Request length | Ordinarily no more than 500 words excluding annexures and addresses; excess length alone is not a rejection ground | 2016 Rule 5(1) |
| BPL treatment | No application or additional information fee; BPL proof required | RTI Act Section 7(5), Haryana guidance and portal flow |
| Offline payment | Cash against receipt, bank draft, Indian Postal Order, or treasury challan | Haryana Rules and Model Form B |
| Online payment | Net banking, credit/debit card, UPI, NEFT, RTGS, or e-Challan; e-Challan may be paid by cheque or cash at SBI | Haryana RTI portal |
| Application form | Model Form A is preferred under Rule 3(1), rather than treated as an exclusive statutory format | Haryana Rules, 2009, as amended |
| Identity evidence | Required: Aadhaar, passport, voter card, PAN, Parivar Pehchan Patra ID, or another government-issued identity card | Replacement Model Form A in the 12 Apr 2021 amendment; 20 May 2024 compliance circular |
| Portal fields | Subject up to 1,000 characters; description up to 5,000 characters | Current Haryana citizen manual |
| Portal attachment | PDF up to 20 MB | Current Haryana citizen manual |
| First-appeal fee | ₹0 | Current Haryana citizen manual |
| First-appeal evidence | Application/enclosures, PIO acknowledgement, postal proof, and PIO decision when available | Current Haryana citizen manual |
| Second appeal | Not supported for drafting in v1; portal currently directs manual filing in triplicate | Haryana portal and Rule 6 |

## Identity-document safety

Haryana is the only currently researched MVP jurisdiction with an express general identity-document field. SunwaiSaathi must not hide or omit that requirement, but it must minimise the privacy risk:

1. explain that an accepted government-issued identity document is required for a Haryana state filing;
2. process any identity image or PDF locally only;
3. never transmit or retain the document on a SunwaiSaathi server;
4. never include its number in analytics, logs, URLs, filenames, crash reports, or generated plain-text previews;
5. keep the identity attachment separate from the RTI request text and public project fixtures;
6. warn users that redaction may cause rejection unless the receiving authority accepts the redacted proof; and
7. provide a manual-attachment path so the document need not enter the application at all.

The product must not recommend one accepted ID over another as legally safer without reviewed official guidance.

## Amendment history

| Date | Instrument | Filing consequence |
|---|---|---|
| 21 Dec 2009 / 1 Jan 2010 | Haryana Right to Information Rules, 2009; effective 1 Jan 2010 | State procedure and model forms |
| 18 Mar 2016 | Haryana RTI Amendment Rules, 2016 | ₹10 fee, ordinary 500-word rule and revised information charges |
| 3 Jul 2018 | Rule 10 amendment | Commission penalty procedure; no application-field change identified |
| 12 Apr 2021 | Haryana RTI Amendment Rules, 2021 | Replacement Model Form A adds accepted identity-document field |
| 20 May 2024 | General Administration compliance circular | Directs Haryana authorities to enforce the 2021 identity-proof requirement |

## Review gates

1. Obtain legal/RTI approval for the consolidated 2009–2024 interpretation.
2. Confirm whether every supported authority accepts every Rule 4 payment mode and how instruments must be drawn.
3. Verify live portal coverage and whether a first appeal is limited to applications originally filed online.
4. Select 5–10 authorities and verify designation-based PIO/FAA sources.
5. Add tests for ₹10, 500 words, mandatory identity evidence, 1,000/5,000-character fields, 20 MB PDFs, and zero first-appeal fee.
6. Add security tests proving identity files never enter logs, network calls, source control, or public fixtures.

Until these gates pass, the Haryana structured profile remains `research` and cannot produce output labelled filing-ready.
