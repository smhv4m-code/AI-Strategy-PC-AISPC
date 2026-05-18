# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |
| | | H / M / L |

### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |
| | | H / M / L |

### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |

## Board Pitch
**Thesis (1 sentence):**
We should invest in AI-driven workflow orchestration inside SAP SuccessFactors now because enterprise HR teams are already automating critical processes outside governed systems, and we can convert that unmanaged operational risk into a defensible platform capability with measurable efficiency and compliance gains.

**The case:**
1. Why now: Enterprise HR organizations have crossed from experimentation into operational AI usage in the last 6–12 months, but most adoption is happening through unmanaged “shadow AI” workflows rather than inside core systems. Our audit already identified 27 shadow workflows and an estimated $180K–$350K in adjacent unmanaged spend. At the same time, customers are demanding faster approvals, lower operational overhead, and more intelligent workflow routing without increasing HR headcount. The timing matters because orchestration — not generic copilots — is becoming the control layer customers are willing to operationalize. If we do not own that layer inside SuccessFactors, customers will assemble it externally through point tools and automation vendors.

2. What's defensible: The moat is not the model — it is the workflow graph, correction history, approval behavior, and enterprise policy context accumulated through orchestration. The strongest emerging asset is the workflow correction loop: user overrides, approval edits, rejected workflows, and escalation paths continuously improve orchestration accuracy over time. That creates switching costs competitors cannot quickly replicate with generic models alone. The current moat posture is credible but not complete: Data advantage is strong (4/5), platform leverage is moderate (3/5), and vendor portability remains partial, which means speed of execution matters. The biggest encroachment threat is a platform vendor shipping “good enough” orchestration bundled into their suite before we establish workflow-level reliability and trust.

3. The economics: The economic profile only works if orchestration is tiered aggressively by workflow complexity. The strategy already reflects the right structure: lightweight models handle routing, intent detection, FAQs, and low-risk approvals; expensive frontier reasoning is reserved for high-risk organizational decisions and multi-step ambiguity. That keeps AI cost concentrated on high-value workflows rather than broad conversational traffic. The pricing model also aligns with where enterprise SaaS is moving: seat-based licensing expands into execution-based monetization tied to workflow volume and autonomous actions. The margin risk is real because orchestration systems can become inference-heavy very quickly at scale, but the architecture choice here intentionally protects gross margin by limiting frontier model exposure to a small percentage of traffic. The current strategy is directionally strong, but several economics assumptions remain unproven and need validation in Horizon 2 before broader rollout.

**The risks:**
1. Trust / failure modes: The highest-risk scenario is not a bad chatbot answer — it is an autonomous workflow making a materially wrong HR decision with legal, compensation, or employee-relations impact. We already identified concrete failure modes: policy hallucinations in partially ingested countries, workflow confusion around future-dated job changes, and ambiguity during onboarding-to-hire transitions. The mitigation strategy is appropriately conservative: confidence thresholds, explainability layers, human escalation for high-risk actions, workflow-level auditability, and hard autonomy boundaries around terminations, executive approvals, compensation thresholds, and cross-country policy conflicts. The reliability target is >94%, and the stated kill criteria — below 90% accuracy — is correct and should remain enforced.

2. Scale / governance: At 10x usage, three things break first: governance, operational cost control, and workflow sprawl. Without strong boundaries, orchestration systems drift from “assistant” into unmanaged decision-making infrastructure. The proposed governance posture is sound because it treats the system as AI-assisted enterprise workflow orchestration rather than unrestricted autonomy. Weekly reliability reviews, audit cadence, escalation triggers, and layered agent boundaries are necessary operating mechanisms, not compliance theater. The compounding loops are promising, but at least one remains weak today: the organization has not yet proven that workflow corrections reliably improve orchestration quality at scale without introducing drift or regression.

3. Competitive: The kill scenario is straightforward: if bundled platform competitors achieve comparable workflow reliability and approval automation before we establish measurable operational advantage, this becomes feature parity rather than strategic differentiation. That is why the first 6 months matter. If we cannot sustain >90% workflow accuracy, demonstrate measurable reduction in manual approvals/escalations, and prove customers trust the orchestration layer in production workflows, the program should be stopped before scaling investment further.

**The ask:**
Requesting $500K, 5 engineers, and 1 product manager over a 6-month horizon to validate AI orchestration as a platform capability inside SuccessFactors workflows. The immediate outcome is not a generalized AI assistant — it is a production-grade orchestration layer focused on measurable workflow acceleration, governed autonomy, and operational trust. Funding this means deprioritizing lower-leverage incremental UX enhancements and non-strategic automation requests in the near term so the team can concentrate on establishing workflow reliability, governance infrastructure, and enterprise trust before competitors normalize the category.
**Now:**
