# SPEC_02_SAMPLE_DATA.md
**Project:** Mizuho CIB — Banker Assistant Agent POV
**Component:** Sample Data — Demo Scenario
**Demo Flow(s):** Flow A (Morning to Meeting)
**Org Alias:** `Mizuho CIB`
**API Version:** 61.0
**Status:** Not Started

---

## Overview

> Loads the demo scenario data — a Singapore-based RM covering multi-market corporate clients. Includes client accounts (with entity hierarchies), contacts (decision-makers), financial accounts (loans, FX, trade finance), portfolio signals, covenant alerts, and upcoming meeting context.

---

## Dependencies

### Must be deployed before this
| Spec | Component | Why |
|---|---|---|
| SPEC_00 | Permission Sets | Data scripts run as permissioned user |
| SPEC_01 | Data Model | Objects and fields must exist before data load |

### What depends on this
| Spec | Component | Why |
|---|---|---|
| SPEC_03 | Agentforce Agent | Agent needs data to generate briefings |
| SPEC_04 | Client Briefing LWC | LWC displays loaded data |
| SPEC_05 | Meeting Notes Flow | Flow references meeting and contact records |

---

## Technical Design

> *To be filled during build phase.*

---

## Metadata / Code

> *To be filled during build phase.*

---

## Deployment

```bash
sf apex run --target-org "Mizuho CIB" --file scripts/apex/loadSampleData.apex
```

---

## Testing

1. [ ] Client accounts created with correct entity hierarchy
2. [ ] Contacts linked with appropriate roles (Treasurer, CFO, etc.)
3. [ ] Financial accounts show multi-product wallet (loans, FX, treasury)
4. [ ] Portfolio signals and alerts present for demo scenario
5. [ ] Upcoming meeting record exists for today's demo flow

---

## Acceptance Criteria

- [ ] Minimum 3 corporate client accounts with entity hierarchies
- [ ] At least 1 client has a covenant alert triggering the morning briefing
- [ ] Cross-sell signal visible (e.g. FX hedging opportunity from loan maturity)
- [ ] Demo scenario runs end-to-end with loaded data
