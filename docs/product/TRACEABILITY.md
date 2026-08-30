# MVP Traceability Matrix

**Status:** Initial Milestone 1 framework

| Requirement | Source/evidence | Planned implementation | Acceptance evidence |
|---|---|---|---|
| Five independent jurisdictions | `SPEC.md` §5; jurisdiction dossiers | Versioned jurisdiction profiles | Cross-jurisdiction routing tests |
| Primary-source-only legal behavior | `SPEC.md` §8.2; `SOURCE_INVENTORY.md` | Source schema and approval status | Schema checks and reviewer record |
| Standard 30-day clock only | Current RTI Act Section 7(1); [deadline contract](./DEADLINES_AND_FIRST_APPEALS.md) | Receipt-event deadline module | Boundary and confidence-label tests |
| First appeal | Current RTI Act Sections 19(1)/(6); [six-category contract](./DEADLINES_AND_FIRST_APPEALS.md) | Six reviewed appeal modules | Branch-complete zero-critical suite |
| Officer clause optional | Current Sections 8(1)(j)/8(2), pending legal review | Unchecked protected module | Mandatory caveat regression test |
| State-aware fees/forms/routes | Five official jurisdiction dossiers | Deterministic rule lookup | Per-jurisdiction golden fixtures |
| No invented authority/address | Current official authority sources | Approved directory; generic fallback | Missing/stale address tests |
| English and Hindi output | `SPEC.md` §§10, 17 | Independently reviewed templates | Legal and language approvals |
| Local document processing | `SPEC.md` §§10.3–10.4 | Browser parsing/OCR/redaction | Network and hostile-file tests |
| Anonymous, local-first use | `SPEC.md` §§13–14, 18 | Static-first PWA and encrypted opt-in save | Offline/privacy-boundary tests |
| Calendar reminder | `SPEC.md` §11 | Local `.ics` generator | Calendar compatibility tests |
| AI cannot override law | `SPEC.md` §15.4 | Typed extraction boundary and precedence | Conflict and prompt-injection tests |
| Zero critical legal errors | `SPEC.md` §16.3 | Safety-weighted grader/release gate | Published release evaluation |
| WCAG 2.2 AA | `SPEC.md` §17 | Accessible component/system design | Automated and manual audit |
| Zero incremental cost | `SPEC.md` §§3, 14.3 | Static deployment; Hostinger candidate | Hosting decision ADR and invoice-free operation |
