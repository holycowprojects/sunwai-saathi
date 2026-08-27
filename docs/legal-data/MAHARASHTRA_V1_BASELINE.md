# Maharashtra v1 Legacy Baseline

**Dataset version:** `2026.08.6`

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
| Offline application payment | Cash against receipt, demand draft, Indian Postal Order, banker's cheque, or ₹10 court-fee stamp | Rule 3 of the 2005 Rules, amended in 2013 |
| Subject scope | One subject matter per request | Rule 3A inserted by the 16 Jan 2012 amendment |
| Request length | Ordinarily no more than 150 words | Rule 3A inserted by the 16 Jan 2012 amendment |
| Record inspection | Supervised during office hours; pencil only; no marking of records | Rule 3B inserted by the Second Amendment Rules, 2012 |
| Portal overflow | Text over 150 words may be attached as PDF up to 1 MB | Official citizen manual |
| Online application payment | Net banking or major debit/credit cards | Official citizen manual and current portal |
| First-appeal fee | ₹20 | Official SIC format and Maharashtra RTI Online FAQ |
| Offline first-appeal payment | Cash against receipt, demand draft, Indian Postal Order, banker's cheque, or ₹20 court-fee stamp | Rule 5 of the 2005 Rules, amended in 2013 |
| First-appeal evidence | Copies of the original application and papers submitted to or received from the PIO | Official SIC format |
| Online first appeal | Original registration number; PDF supporting document up to 1 MB; net banking or major cards | Official citizen manual and portal FAQ |
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
| `MH-RTI-SECOND-AMEND-2012-INSPECTION` | 2 Feb 2012 | 4,011,481 | `c9b81cf4c3a39a166e37ae68204272097bcdb4d8bceb3df680c5b0ce25de554a` |
| `MH-RTI-NOTIFICATION-2013-FEE-FORM` | 23 Apr 2013 | 25,468 | `143bc0fb775cfc1290db822aeaf4388a4032a42fb0e2d3daf9d3f4ae670fead6` |
| `MH-RTI-FORMAT` | Publication date unavailable | 1,838,760 | `54d6bf0a6ebe1f1af0014d3a10483f44786fab079d48a32c8028ace3e6ef0f84` |
| `MH-PORTAL-FAQ` | Publication date unavailable | 204,747 | `6a3269588e94bda51f4b40150aaeb4571deabcf569db849681452826be3fec6f` |
| `MH-PORTAL-MANUAL` | Publication date unavailable | 4,368,976 | `ee3ba7304bfd6d30c067597df449386cb0c25cdee48b39a52aff841f03a41f17` |

## Unresolved review gates

1. Obtain independent Marathi and legal/RTI review of the direct visual transcription of the 23 April 2013 notification.
2. Confirm that using current operational portal instructions does not import a requirement introduced only by the deferred 2026 instruments.
3. Have an identified legal/RTI reviewer approve the baseline.
4. Add automated tests for one-subject scope, the ordinary 150-word ceiling, Indian Postal Order support, ₹10 application fee, ₹20 first-appeal fee, and absence of a default photo-ID demand.

Until these gates pass, structured data must remain `research`, and the application must not label Maharashtra output filing-ready.
