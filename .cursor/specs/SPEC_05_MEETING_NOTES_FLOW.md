# SPEC_05_MEETING_NOTES_FLOW.md
**Project:** Mizuho CIB — Banker Assistant Agent POV
**Component:** Flow: Post-Meeting Auto-Capture
**Demo Flow(s):** Flow A (Morning to Meeting)
**Org Alias:** `Mizuho CIB`
**API Version:** 61.0
**Status:** Not Started

---

## Overview

> An automation that triggers post-meeting to capture meeting notes (from agent transcript or RM input), assign follow-up tasks to the appropriate team members, schedule next steps, and log the interaction to CRM — eliminating the manual data entry that bankers currently despise.

---

## Dependencies

### Must be deployed before this
| Spec | Component | Why |
|---|---|---|
| SPEC_00 | Permission Sets | Flow execution requires permission |
| SPEC_01 | Data Model | Flow writes to custom objects (tasks, activities) |
| SPEC_02 | Sample Data | Flow references meeting and contact records |
| SPEC_03 | Agentforce Agent | Agent invokes this flow |

### What depends on this
| Spec | Component | Why |
|---|---|---|
| SPEC_06 | Lightning Page | Meeting history visible on page |

---

## Technical Design

> *To be filled during build phase.*

---

## Metadata / Code

> *To be filled during build phase.*

---

## Deployment

```bash
sf project deploy start \
  --target-org "Mizuho CIB" \
  --source-dir "force-app/main/default/flows"
```

---

## Testing

1. [ ] Flow activates without errors
2. [ ] Meeting notes record created after agent captures notes
3. [ ] Follow-up tasks assigned to correct users
4. [ ] Activity logged on the Account/Contact timeline
5. [ ] No duplicate records on re-run

---

## Acceptance Criteria

- [ ] Flow triggers from Agentforce agent action
- [ ] Meeting summary stored as a structured record (not free text blob)
- [ ] At least 2 follow-up tasks auto-created with due dates
- [ ] Activity appears in Account timeline within 5 seconds
- [ ] Flow handles missing data gracefully (no unhandled fault)
