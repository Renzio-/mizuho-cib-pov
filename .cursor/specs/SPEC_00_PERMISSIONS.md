# SPEC_00_PERMISSIONS.md
**Project:** Mizuho CIB — Banker Assistant Agent POV
**Component:** Permission Sets & Profiles
**Demo Flow(s):** Flow A (Morning to Meeting)
**Org Alias:** `Mizuho CIB`
**API Version:** 61.0
**Status:** Not Started

---

## Overview

> Defines the permission sets required for the Banker Assistant Agent POV — covering RM access to custom objects, Agentforce agent invocation, and LWC component visibility.

---

## Dependencies

### Must be deployed before this
| Spec | Component | Why |
|---|---|---|
| None | — | This is the first deployment |

### What depends on this
| Spec | Component | Why |
|---|---|---|
| SPEC_01 | Data Model | Custom objects require permission set assignment for field access |
| SPEC_02 | Sample Data | Data loading scripts run as a user with these permissions |
| All subsequent | All components | LWCs, Flows, and Agents require permission sets |

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
  --source-dir "force-app/main/default/permissionsets"
```

---

## Testing

1. [ ] Permission sets visible in Setup → Permission Sets
2. [ ] Assign permission set to demo user
3. [ ] Demo user can access all custom objects
4. [ ] No permission errors in browser console during demo flow

---

## Acceptance Criteria

- [ ] Permission sets deploy without errors
- [ ] Demo user has full CRUD on all custom objects
- [ ] Agentforce agent invocation permission granted
- [ ] LWC components visible to assigned users
