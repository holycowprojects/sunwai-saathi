# Milestone 1 Risk Register

| ID | Risk | Likelihood | Impact | Mitigation | Exit evidence |
|---|---|---:|---:|---|---|
| `L-01` | Official sites expose obsolete state RTI laws beside current material | High | Critical | Explicit `superseded` state; Gazette/India Code precedence; legal review | Delhi and Goa legacy-law notes resolved |
| `L-02` | A portal instruction conflicts with operative rules | Medium | High | Record conflict; separate legal rule from portal operation; block filing-ready status | Signed conflict resolution record |
| `L-03` | Maharashtra fee claim is based on secondary reporting or incomplete PDF extraction | High | Critical | Do not encode ₹30 until operative 2026 rule text is captured and reviewed | Primary provision and checksum |
| `L-11` | Published Maharashtra 2026 rules conflict with reports that implementation was stayed | High | Critical | V1 uses only a verified pre-June-2026 baseline and clearly versions it; reassess the 2026 rules in v2 | Reviewed pre-June baseline for v1; official status instrument before any v2 change |
| `L-12` | Treating the single-subject/150-word constraint as a 2026-only change would generate non-compliant legacy-baseline drafts | High | High | Encode the 2012 Rule 3A constraint in Maharashtra v1 and test every generated request | Reviewed 2012 notification plus word-count and subject-scope tests |
| `L-04` | Section 8(1)(j) caveat overstates privacy exemption | Medium | High | Review current Act as a whole; avoid categorical result; optional clause | Legal/RTI-approved wording |
| `L-05` | Official authority/FAA details change frequently | High | High | Store roles not names; freshness metadata; no verified address means no filing-ready address | Current authority source per entry |
| `L-06` | Government pages are unavailable or silently replaced | High | Medium | URL metadata, SHA-256 capture, monthly health checks, change review | Reproducible capture log |
| `L-07` | No qualified volunteer legal/RTI reviewer is available | Medium | Critical | Keep affected output unreviewed/non-filing-ready; recruit before public beta | Named reviewer and approval record |
| `L-08` | Official grievance statistics are inadequate for authority ranking | Medium | Medium | Publish fallback scoring rubric and evidence for every criterion | Scored candidate table |
| `L-09` | Delhi is incorrectly routed through the Central portal | Medium | Critical | Independent profiles and critical evaluation case | Passing routing tests |
| `L-10` | Research scope expands to exceptional timing or second appeals | Medium | Medium | Enforce supported-case matrix and TODO boundary | Traceability review |
