# Supported-Case Matrix

**Status:** Draft for Milestone 1 review

| Scenario | MVP status | Product behavior |
|---|---|---|
| Existing grievance; standard RTI request for records; supported authority and verified jurisdiction data | Supported | Filing-ready draft and submission pack |
| Existing grievance; supported jurisdiction but unsupported authority | Partial | Generic draft; no unverified postal address or FAA details |
| General RTI not tied to an existing grievance | Unsupported | Explain scope; do not generate filing-ready output |
| Central authority filed through Central portal | Supported after profile review | Use Central profile only |
| GNCT Delhi authority | Supported after profile review | Use Delhi profile; never route to Central portal |
| Haryana, Maharashtra or Goa state authority | Supported after profile review | Use its independent state profile |
| Maharashtra authority in v1 | Supported after pre-June baseline review | Generate filing-ready output from verified pre-June-2026 rules; exclude disputed 2026 fee, ID, restriction, and form changes; stamp the baseline and review date |
| Life-or-liberty request | Unsupported in MVP | Explain exceptional 48-hour path and recommend independent assistance |
| APIO filing, Section 6(3) transfer, third-party consultation, exempt organization or additional-fee timing | Unsupported timing | Do not calculate a filing-ready deadline |
| Standard date based on confirmed PIO/public-authority receipt | Supported | Label deadline confirmed |
| Only submission date known | Supported with limitation | Label deadline estimated and explain basis |
| Officer identity/designation request | Optional | Separate unchecked reviewed clause and amended Section 8(1)(j) caveat |
| No PIO response after standard period | First appeal supported | Use reviewed no-response module |
| Incomplete response | First appeal supported | Use reviewed incomplete-information module |
| Incorrect or misleading response | First appeal supported | Use reviewed incorrect/misleading module |
| Explicit refusal | First appeal supported | Use reviewed refusal module; user confirms cited provision |
| Excessive fee | First appeal supported | Use reviewed excessive-fee module |
| Other first-appeal issue | Bounded support | User selects reviewed modular grounds; no open-ended AI legal argument |
| Second appeal | Unsupported | Provide limitation only; do not draft or estimate disposal time |
| Address or FAA not verified | Not filing-ready | Generate generic content and direct user to official directory |
| Legal data over six months since review | Supported with warning | Require acknowledgement and stamp review/version details |
| Newer legal dataset available to installed PWA | Draft only until update | Block new filing-ready export until data refresh |
| Device cannot perform OCR/local AI | Supported fallback | Manual deterministic form remains available |
