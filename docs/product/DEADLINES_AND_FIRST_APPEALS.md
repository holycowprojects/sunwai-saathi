# Deadline and first-appeal contracts

**Status:** Initial technical product contract; requires legal/RTI review

**Legal-data baseline:** `2026.08.2`

**Last reviewed:** 30 August 2026

This contract turns the verified national statutory baseline into deterministic product behavior. It does not add jurisdiction-specific rules, court-holiday adjustments or legal advice.

## Standard 30-day calculation

The MVP calculates only the ordinary Section 7(1) response target for a request received directly by the relevant public authority or PIO.

### Required input

| Field | Allowed value | Consequence |
|---|---|---|
| `eventDate` | Valid calendar date | Date from which the target is calculated |
| `eventType` | `confirmed-receipt` or `submission-proxy` | Determines confidence label |
| `submissionRoute` | `online`, `post`, or `in-person` | Supports the basis explanation; does not alter the 30 days |
| `userConfirmed` | `true` | No result before the user confirms the displayed date and event |
| `exceptionFlags` | Explicit booleans for every unsupported timing branch | Any true flag blocks a calculated target |

### Calculation

`statutoryTargetDate = eventDate + 30 calendar days`

The receipt date is day zero. The result is an unadjusted statutory target, not a guaranteed response date. The MVP does not move a target that falls on a weekend or public holiday because no reviewed adjustment rule is currently encoded.

### Confidence labels

- `confirmed`: used only when the user has evidence of the date the relevant public authority or PIO received the request, such as an official portal acknowledgement, receiving stamp or delivery confirmation.
- `estimated`: used when the relevant receipt date is unknown and the user explicitly confirms a submission date as a proxy. The output states that actual receipt may have occurred later and asks the user to replace the proxy when receipt evidence becomes available.
- `not-calculated`: used when the date is missing/unconfirmed or an exceptional timing flag applies.

Online submission is not automatically confirmed receipt. The acknowledgement must show acceptance/receipt by the relevant authority. A postal dispatch date alone can produce only an estimate, never a confirmed target.

### Output contract

Every displayed or exported result contains:

- the input date;
- its event type and submission route;
- `confirmed`, `estimated`, or `not-calculated` confidence;
- the unadjusted 30-calendar-day target when calculated;
- a statement that the date is the ordinary RTI response target, not a promise of grievance resolution;
- the application and legal-data versions; and
- the relevant warning or unsupported reason.

The calculator does not decide that a legal deadline has conclusively expired. A user must confirm the dates again before generating a no-response first appeal.

## Detected but unsupported timing branches

The intake must ask enough questions to detect these branches before calculation. If any applies, it returns `not-calculated`, preserves the user's facts locally and gives a plain-language reason.

| Flag | Detected when | MVP behavior |
|---|---|---|
| `life-or-liberty` | User says the request invokes the 48-hour life-or-liberty route | Do not calculate; explain that urgent specialist assistance may be appropriate |
| `filed-through-apio` | Request was submitted through an Assistant PIO | Do not add or guess an adjusted period |
| `section-6-3-transfer` | Any part was transferred between public authorities | Do not infer which receipt event controls |
| `third-party-procedure` | A notice or decision invokes third-party consultation | Do not calculate an adjusted target |
| `exempt-organisation` | Authority relies on the exempt-organisation framework | Do not calculate a standard target |
| `additional-fee-notice` | PIO requested further fee or communicated a fee calculation | Do not subtract, pause or restart time |
| `multiple-or-unclear-receipts` | More than one plausible receipt date exists | Require clarification; otherwise do not calculate |

Detection is not a legal classification. The interface says why the standard calculator is unavailable and does not recommend whether the user should appeal.

## First-appeal shared inputs

All six branches require:

- jurisdiction and selected public authority;
- original RTI registration/reference number, when issued;
- copy or user-confirmed summary of the original request;
- original submission date and confirmed receipt date when available;
- submission route;
- selected outcome category confirmed by the user;
- the application and legal-data versions; and
- a verified FAA office/designation/address for filing-ready output.

If the FAA record is missing, stale or unapproved, the product may generate generic appeal content but must block a filing-ready address and clearly direct the user to the official directory. Uploaded replies remain local. Suggested extracted facts never become final until the user confirms them.

## Six bounded outcome categories

### 1. No response

Additional inputs:

- ordinary response target and its confidence;
- user confirmation that no decision or information was received by the chosen appeal date; and
- confirmation that no unsupported timing flag applies.

Filing-ready behavior requires a confirmed receipt basis. An estimated target may prepare a draft, but the product warns that the appeal's timing basis needs verification.

### 2. Incomplete information

Additional inputs:

- PIO decision/reply date and actual receipt date;
- user-selected original request points not answered; and
- description of records supplied, if any.

The product maps omissions to the user's original numbered requests. It does not invent missing records or claim that a record must exist.

### 3. Incorrect or misleading information

Additional inputs:

- PIO decision/reply date and actual receipt date;
- exact disputed statement or supplied record selected by the user; and
- user-provided reason or record showing the apparent inconsistency.

The output describes the inconsistency and asks for the relevant existing records. It does not accuse an officer of misconduct or assert falsity as an established fact.

### 4. Refusal

Additional inputs:

- PIO decision/reply date and actual receipt date;
- refused original request points; and
- exemption/provision exactly as stated in the reply, or `not-stated`, confirmed by the user.

Only reviewed modular grounds may be used. The product never fabricates a cited exemption or unrestricted public-interest argument.

### 5. Excessive fee

Additional inputs:

- fee-notice date and actual receipt date;
- amount demanded and calculation stated by the PIO;
- affected request points and described format/volume; and
- whether a BPL exemption was claimed, with no unnecessary identity data retained.

Because additional-fee timing is outside the calculator, this branch does not generate an adjusted Section 7 deadline. Grounds are limited to reviewed fee-rule comparisons for the selected jurisdiction.

### 6. Other issue

Additional inputs:

- PIO decision/reply date and actual receipt date, if any;
- one or more user-selected grounds from a reviewed allowlist; and
- facts required by each selected module.

There is no free-form AI legal-ground generator. If no reviewed module fits, the case is unsupported for filing-ready output and the product may export only the user's factual notes.

## First-appeal timing display

For a no-response branch, the Section 19(1) filing-window basis is the expiry of the ordinary response period. For a decision-based branch, it is the actual date the applicant received the decision. The interface identifies which basis it uses and calculates a 30-calendar-day target only after the relevant date is confirmed.

Delayed appeals may be admitted for sufficient cause, but SunwaiSaathi does not decide sufficiency. The Section 19(6) 30-day disposal period, extendable to a total of 45 days for recorded reasons, is displayed as a statutory appeal-disposal period—not a promised result or grievance-resolution timeline.

Second appeals remain outside the MVP.

## Release tests implied by this contract

- Leap day, month-end and year-end date arithmetic
- Receipt date as day zero and exactly 30 calendar days later
- Confirmed, estimated and not-calculated labels
- Every unsupported exception independently blocks calculation
- Multiple exception flags remain blocking
- Central and Delhi stay separate
- Missing/stale FAA prevents a filing-ready address
- Each appeal category requires its branch-specific inputs
- Extracted dates, provisions and categories require user confirmation
- No-response estimated basis cannot silently become filing-ready
- Additional-fee branch never emits an adjusted deadline
- No output promises RTI, appeal or grievance resolution
