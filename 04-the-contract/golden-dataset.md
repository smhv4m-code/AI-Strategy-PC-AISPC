# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | Employee promotion request with policy-compliant salary increase | Approve workflow and generate compensation recommendation | N | rule |
| 2 | Future-dated hire created through Onboarding 2.0 MPH scenario | Correctly identify employee state and trigger downstream workflow | Y | rule |
| 3 | Employee asks conflicting leave policy question across two regions | Return region-specific policy with clarification prompt | Y | LLM |
| 4 | Uploaded HR document missing mandatory fields | Detect missing fields and escalate for review | Y | rule |
| 5 | Manager requests termination outside policy threshold | Reject recommendation and trigger HRBP approval escalation | Y | LLM |

**Adversarial rows included:**  
- Contradictory HR policies  
- Ambiguous manager intent  
- Incomplete onboarding payloads  
- Prompt injection attempts in uploaded documents  
- Multi-region policy conflicts  
- Role spoofing attempts  

**Coverage gaps identified by partner:**  
- Cross-module workflow edge cases  
- Country-specific labor law interpretation  
- Extremely large organizational hierarchy reasoning  
- SAP API timeout/retry failure behavior  
- Multi-language policy interpretation consistency  

---

## Confidence UX Design

**Approach:**  
Tiered confidence model with explainability layer and automatic human-in-the-loop escalation for high-risk workflows

### High confidence (>90%)
- Auto-execute low-risk workflow
- Show concise rationale
- Allow optional human override
- Green confidence indicator

### Medium confidence (70–90%)
- Require user confirmation before execution
- Show reasoning summary and referenced policy
- Highlight ambiguous fields
- Yellow confidence indicator

### Low confidence (<70%)
- Block autonomous execution
- Trigger human review workflow
- Surface uncertainty explanation
- Red confidence indicator

### User control surface
- Confidence score visibility
- “Why was this recommended?” explanation
- Manual override capability
- Escalate to HRBP button
- View audit trail and source policy references
- Rollback/reversal workflow for executed actions

---

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | >94% | Golden dataset evaluation | <91% |
| Hallucination rate | <2% | Human-reviewed sampled outputs | >5% |
| Latency (p95) | <4 seconds | End-to-end workflow timing | >7 seconds |
| Drift velocity | <3% monthly variance | Weekly benchmark comparison | >7% deviation |
| Autonomous execution success rate | >97% | Workflow completion monitoring | <93% |
| Escalation precision | >90% | Correct HITL escalation rate | <85% |

---

## HITL Architecture

### Human Escalation Triggers
- Compensation changes above threshold
- Legal or policy ambiguity
- Low confidence outputs (<70%)
- Executive-level workflows
- Termination workflows
- Cross-country policy conflicts
- Model disagreement scenarios

### Escalation Path
1. AI agent generates recommendation
2. Confidence scoring engine evaluates risk
3. High-risk workflows routed to HRBP or approver
4. Human decision captured as reinforcement signal
5. Audit log stored for governance and retraining

### Human Roles
- HRBP → policy and employee relations review
- Recruiter → hiring validation
- Compensation specialist → salary approvals
- System admin → workflow exception handling

---

## Red-Team Findings

### Failure Modes Identified by Partner
- AI confidently generated policy interpretations for countries with incomplete policy ingestion
- Workflow hallucination occurred when employee had future-dated job changes combined with pending transfers
- Prompt injection attempts inside uploaded onboarding documents manipulated recommendation summaries
- Cross-region compensation benchmarking created invalid salary recommendations
- Ambiguous approval hierarchies caused incorrect autonomous routing

### Mitigations Implemented
- Mandatory policy source citation layer
- Confidence degradation on incomplete retrieval
- Document sanitization pipeline
- Hierarchy validation checkpoints
- Human approval requirement for compensation-sensitive actions
- Multi-model consensus checks for high-risk workflows
