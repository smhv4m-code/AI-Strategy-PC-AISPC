# Cost Curve & Pricing Strategy

# Packaging Decision Model

Leader: Autonomous HR workflow orchestration  
Filler: Conversational copilots, summaries, recommendations  
Killer: AI agents executing real HR transactions autonomously  
Killer Usage %: 18–25% of enterprise users become heavy automation users  
Bundle or Ad-On: Copilot bundled, autonomous agents as premium add-on  

---

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $8–14 | Complex HR reasoning, approvals, policy interpretation |
| Inference (cascading/triage) | $1–3 | Intent routing + lightweight tasks via smaller models |
| Infrastructure | $2–4 | Agent orchestration, APIs, queues, observability |
| Data/storage | $0.50–1.50 | Embeddings, audit logs, workflow memory |
| Human-in-the-loop | $2–6 | Escalations for compensation/legal/high-risk workflows |
| Monitoring & Evaluation | $1–2 | Hallucination tracking, evaluation pipelines |
| Security & Governance | $1–3 | Enterprise compliance, RBAC, auditability |
| **Total AI COGS** | **$15.5–33.5** | Margin heavily dependent on routing efficiency |

---

## Cascading Strategy

<!-- Cheap model → frontier model routing logic -->

**Triage model:**  
Lightweight reasoning model for intent detection, FAQ, routing, and low-risk recommendations

**Mid-tier model:**  
Standard enterprise reasoning for summaries, workflow generation, and document parsing

**Frontier model:**  
Used only for complex multi-step reasoning, organizational decisions, compensation/legal ambiguity, and autonomous workflow orchestration

**Routing rule:**  
- FAQ/navigation → small model  
- Workflow assistance → mid-tier  
- Policy ambiguity → frontier  
- Autonomous approvals → frontier + HITL  
- Low confidence → human escalation  

**Expected cascade ratio:**  

| Model Tier | Traffic % |
|---|---:|
| Small model | 68% |
| Mid-tier model | 24% |
| Frontier model | 6% |
| Human escalation | 2% |

---

## Pricing Model

**Current pricing:**  
Traditional enterprise seat-based SaaS licensing

**Proposed AI pricing:**  
Hybrid AI monetization with execution-based expansion revenue

**Model:**  
Hybrid (seat-based + usage-based + outcome-based)

### Pricing Structure

| Product Layer | Pricing |
|---|---|
| AI Copilot | $25–40/user/month |
| Autonomous HR Agents | $0.50–3 per executed workflow |
| Governance & Audit Layer | Enterprise annual contract |
| Premium Reasoning Tier | Usage multiplier |
| Heavy orchestration | Usage-based overages |

---

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | Gross margin drops below 45% | Aggressive cascading, caching, prompt optimization |
| Heaviest segment doubles | Power users become unprofitable | Usage throttling, enterprise tiering |
| Model provider raises prices 50% | Vendor concentration risk | Multi-model abstraction layer |
| Autonomous usage spikes | HITL costs rise sharply | Confidence scoring + approval thresholds |
| Hallucination incident in HR workflow | Enterprise trust damage | Audit trails, explainability layer |
| SAP API limits change | Integration costs increase | Local orchestration caching |

---

## Board One-Pager

### Before (Traditional SaaS)

- Revenue scales with seats
- Predictable infrastructure costs
- Human-driven execution
- Limited workflow intelligence
- High manual HR operations cost

### After (AI-Enabled)

- Revenue scales with intelligence consumption
- Autonomous workflows create expansion revenue
- AI becomes operational layer
- Workflow execution partially automated
- Governance becomes monetizable
- Margin tied to inference optimization efficiency

### Net Margin Shift

| Metric | Traditional SaaS | AI-Native SaaS |
|---|---:|---:|
| Gross Margin | 82–88% | 52–72% |
| Expansion Revenue | Moderate | High |
| Marginal User Cost | Near-zero | Usage-sensitive |
| Differentiation | Features | Workflow intelligence |
| Enterprise Lock-in | Medium | Very high |
| Strategic Moat | UI/process | Memory + orchestration + trust |

---

## Pricing Model Insight

The winning AI pricing strategy is:

> Cheap intelligence assistance, expensive autonomous execution.

Enterprises are more willing to pay for:
- workflow execution
- operational automation
- governance reduction
- decision acceleration
- measurable business outcomes

than for:
- AI conversations
- token consumption
- generic copilots
