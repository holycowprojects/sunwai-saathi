# Maharashtra v1 Legacy Baseline

**Dataset version:** `2026.08.1`

**Technical review date:** 27 August 2026

**Product status:** Research; not filing-ready until legal/RTI approval

**Temporal cutoff:** Rules and amendments applying before the June 2026 publication

## Product policy

SunwaiSaathi v1 keeps Maharashtra in MVP scope. Its filing behavior will use this pre-June-2026 baseline after legal/RTI approval. It will not infer the current legal effect of the Maharashtra Right to Information Rules, 2026 or their 19 June amendment. That reassessment belongs to v2.

This is a versioned product policy, not a legal conclusion that the pre-June rules currently govern every Maharashtra filing.

## Technically verified baseline

| Behavior | v1 value | Primary basis |
|---|---|---|
| Application form | Annexure A prescribed by Rule 3 | Maharashtra Right to Information Rules, 2005 |
| Application fee | ₹10 | Rule 3 of the 2005 Rules |
| Offline application payment | Cash against receipt, demand draft, banker's cheque, or ₹10 court-fee stamp | Rule 3 of the 2005 Rules |
| Subject scope | One subject matter per request | Rule 3A inserted by the 16 Jan 2012 amendment |
| Request length | Ordinarily no more than 150 words | Rule 3A inserted by the 16 Jan 2012 amendment |
| First-appeal fee | ₹20 | Official SIC format and Maharashtra RTI Online FAQ |
| Identity evidence | No general photo-ID requirement encoded | Pre-June Annexure A evidence reviewed so far; the explicit identity field appears in the 19 Jun 2026 replacement form |
| BPL application fee | Exempt, subject to proof of BPL status | RTI Act Section 7(5) proviso and Annexure A |

The drafting engine must count words deterministically and keep each Maharashtra application to one grievance/file subject. If intake contains multiple independent subjects, it must split them into separate drafts or ask the user to narrow the request.

## Excluded from v1

- the claimed ₹30 application fee under the disputed 2026 instruments;
- the photo-identity field added by the 19 June 2026 replacement Annexure A;
- revised 2026 forms and payment rules; and
- any other behavior supported only by the 2026 publication.

The one-subject rule and ordinary 150-word limit are **not** excluded: they date to the 2012 amendment and are part of this legacy baseline.

## Captured official files

The raw PDFs were downloaded to an untracked temporary directory. Only their metadata and hashes belong in Git.

| Source ID | Published | Bytes | SHA-256 |
|---|---:|---:|---|
| `MH-RTI-RULES-2005` | 11 Oct 2005 | 905,576 | `1bb69929e302f2cf844936dc4bc34d4a96899b1295923ae43075035e03a1f4a4` |
| `MH-RTI-AMEND-2012-SINGLE-SUBJECT` | 16 Jan 2012 | 57,444 | `492c8d1a99881c3e93f422f8b8f18dd76cff59b53e7fd35af326598529add63b` |
| `MH-RTI-NOTIFICATION-2013-FEE-FORM` | 23 Apr 2013 | 25,468 | `143bc0fb775cfc1290db822aeaf4388a4032a42fb0e2d3daf9d3f4ae670fead6` |

## Unresolved review gates

1. Obtain an accessible official Gazette copy or independent two-person transcription of the scanned 23 April 2013 fee/form notification.
2. Reconcile all offline payment modes and the first-appeal fee against the complete amendment chain.
3. Verify current portal coverage, attachment limits, and live payment behavior without importing 2026-only legal requirements.
4. Have an identified legal/RTI reviewer approve the baseline.
5. Add automated tests for one-subject scope, the ordinary 150-word ceiling, ₹10 application fee, ₹20 first-appeal fee, and absence of a default photo-ID demand.

Until these gates pass, structured data must remain `research`, and the application must not label Maharashtra output filing-ready.
