# SPEC_03_AGENTFORCE_BANKER_ASSISTANT.md
**Project:** Mizuho CIB — Banker Assistant Agent POV
**Component:** Agentforce Banker Assistant Agent
**Demo Flow(s):** Flow A (Morning to Meeting)
**Org Alias:** `Mizuho CIB`
**API Version:** 61.0
**Status:** Not Started

---

## Overview

> The core Agentforce agent for the demo — the Banker Assistant. Generates AI-powered client briefings before meetings (portfolio signals, covenant alerts, cross-sell triggers), responds to RM queries about their book, and post-meeting captures notes, assigns follow-ups, and logs activity to CRM. This is the highest-ROI entry point for Mizuho's APAC CIB expansion.

---

## Dependencies

### Must be deployed before this
| Spec | Component | Why |
|---|---|---|
| SPEC_00 | Permission Sets | Agent invocation requires permission |
| SPEC_01 | Data Model | Agent topics reference custom objects for grounding |
| SPEC_02 | Sample Data | Agent needs data to generate meaningful briefings |

### What depends on this
| Spec | Component | Why |
|---|---|---|
| SPEC_04 | Client Briefing LWC | LWC may trigger agent actions |
| SPEC_05 | Meeting Notes Flow | Agent invokes this flow post-meeting |
| SPEC_06 | Lightning Page | Agent panel embedded on the page |

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
  --source-dir "force-app/main/default/agentDefinitions"
```

---

## Testing

1. [ ] Agent visible in Setup → Agentforce Agents
2. [ ] Agent responds to "Prepare my briefing for [client]" with relevant data
3. [ ] Agent surfaces covenant alerts and cross-sell triggers
4. [ ] Agent captures meeting notes when prompted
5. [ ] Follow-up tasks created after meeting capture

---

## Acceptance Criteria

- [ ] Banker Assistant Agent deploys and activates without errors
- [ ] Agent generates client briefing using live org data (not hallucinated)
- [ ] Briefing includes: portfolio summary, alerts, cross-sell signals, meeting context
- [ ] Post-meeting: notes logged, tasks assigned, activity recorded
- [ ] Agent response time under 10 seconds for briefing generation
