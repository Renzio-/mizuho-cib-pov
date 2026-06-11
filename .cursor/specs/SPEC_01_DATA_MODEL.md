# SPEC_01_DATA_MODEL.md
**Project:** Mizuho CIB — Banker Assistant Agent POV
**Component:** FSC Data Model & Custom Objects
**Demo Flow(s):** Flow A (Morning to Meeting)
**Org Alias:** `Mizuho CIB`
**API Version:** 61.0
**Status:** Not Started

---

## Overview

> Defines the data model for the Mizuho CIB POV — leveraging FSC standard objects (Account, Contact, FinancialAccount, FinancialDeal) plus custom objects/fields for portfolio signals, covenant alerts, and cross-sell triggers that power the Banker Assistant Agent.

---

## Dependencies

### Must be deployed before this
| Spec | Component | Why |
|---|---|---|
| SPEC_00 | Permission Sets | Field-level security requires permission sets |

### What depends on this
| Spec | Component | Why |
|---|---|---|
| SPEC_02 | Sample Data | Data loading needs objects/fields to exist |
| SPEC_03 | Agentforce Agent | Agent topics reference these objects for grounding |
| SPEC_04 | Client Briefing LWC | Component queries these objects |
| SPEC_05 | Meeting Notes Flow | Flow writes to these objects |

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
  --source-dir "force-app/main/default/objects"
```

---

## Testing

1. [ ] All custom objects visible in Setup → Object Manager
2. [ ] All custom fields present on their respective objects
3. [ ] Lookup/Master-Detail relationships resolve correctly
4. [ ] No deployment errors or warnings

---

## Acceptance Criteria

- [ ] FSC standard objects (Account, Contact, FinancialAccount) configured with required fields
- [ ] Custom objects for portfolio signals and alerts deploy without errors
- [ ] Object relationships match the SDD architecture diagram
- [ ] All fields accessible to the demo user via SPEC_00 permission sets
