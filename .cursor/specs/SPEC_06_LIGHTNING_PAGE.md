# SPEC_06_LIGHTNING_PAGE.md
**Project:** Mizuho CIB — Banker Assistant Agent POV
**Component:** Lightning App Page: RM Client View
**Demo Flow(s):** Flow A (Morning to Meeting)
**Org Alias:** `Mizuho CIB`
**API Version:** 61.0
**Status:** Not Started

---

## Overview

> The demo Lightning page that brings everything together — the RM's Client 360 view with the Banker Assistant agent panel, client briefing LWC, portfolio overview, meeting history, and Agentforce copilot sidebar. This is the single screen the audience sees during the demo.

---

## Dependencies

### Must be deployed before this
| Spec | Component | Why |
|---|---|---|
| SPEC_00 | Permission Sets | Page assignment requires permission set |
| SPEC_01 | Data Model | Page references custom objects in related lists |
| SPEC_03 | Agentforce Agent | Agent panel embedded on page |
| SPEC_04 | Client Briefing LWC | Component placed on page |
| SPEC_05 | Meeting Notes Flow | Meeting history component on page |

### What depends on this
| Spec | Component | Why |
|---|---|---|
| None | — | This is the final assembly |

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
  --source-dir "force-app/main/default/flexipages"
```

---

## Testing

1. [ ] Page loads without errors on the demo Account record
2. [ ] All LWC components render correctly
3. [ ] Agentforce copilot panel visible and functional
4. [ ] Page layout is clean and demo-ready (no empty sections)
5. [ ] Page assigned as default for the demo user's app

---

## Acceptance Criteria

- [ ] Lightning page deploys and activates without errors
- [ ] All 3 sections of the demo flow visible on one screen
- [ ] Agent panel responds to prompts from the page context
- [ ] No scroll required to see key demo elements (above the fold)
- [ ] Page loads in under 5 seconds on demo org
