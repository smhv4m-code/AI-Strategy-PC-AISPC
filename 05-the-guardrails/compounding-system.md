# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Workflow correction loop | User corrections, approval overrides, rejected workflows | Improved orchestration logic and routing accuracy | Y | active |
| Policy retrieval loop | Updated HR policies, legal changes, SAP configuration updates | Refreshed retrieval embeddings and policy grounding | Y | active |
| Confidence calibration loop | HITL escalations, false positives, hallucination reports | Improved confidence scoring and escalation precision | Y | active |
| Autonomous execution loop | Successful workflow completions and execution telemetry | Optimized automation pathways and reduced friction | Y | active |
| Knowledge fragmentation loop | Team-specific workflows stored in silos | Incomplete organizational reasoning | N | broken |
| Edge-case evaluation loop | Rare workflow failures and exception handling scenarios | Expanded golden dataset coverage | Y | missing |

---

**Broken loop identified by partner:**  
Knowledge fragmentation between HR Operations, HRBP teams, and regional compliance teams prevents organizational reasoning from compounding effectively.

**Fix plan:**  
- Centralized workflow memory layer  
- Shared semantic retrieval index  
- Cross-team policy synchronization  
- Unified audit/event telemetry  
- Continuous edge-case ingestion into golden dataset  
- Monthly governance review for workflow drift  

---

## Context Connectivity

### Current State
Knowledge flows through:
- SAP SuccessFactors workflows
- HR policy repositories
- Ticketing systems
- Email approvals
- Joule AI orchestration layer

### Current Silos
- Regional HR policies
- Compensation exceptions
- Local compliance interpretations
- Legacy onboarding processes
- Manual approval chains

### Connectivity Strategy
- Unified vector memory layer
- Cross-agent shared context store
- Event-driven orchestration
- Organizational graph reasoning
- Policy version synchronization
- Shared confidence scoring system

### Design Principle
> Context must compound across workflows, not reset between interactions.

---

## Governance Policy

**Scope:**  
AI-assisted and autonomous HR workflow orchestration within enterprise HR operations

**Autonomy boundaries:**  
AI may:
- recommend actions
- prepare workflows
- route approvals
- automate low-risk HR transactions

AI may not:
- finalize compensation exceptions
- terminate employees autonomously
- override compliance policies
- execute executive approvals without HITL
- bypass audit logging

**Escalation triggers:**  
- Confidence score below threshold
- Policy ambiguity detected
- Compensation/legal sensitivity
- Cross-region compliance conflicts
- Incomplete employee context
- Prompt injection or anomalous behavior

**Audit cadence:**  
- Weekly reliability review
- Monthly governance review
- Quarterly red-team assessment
- Continuous telemetry monitoring

**Regulatory exposure (EU AI Act / other):**  
- High-risk enterprise workflow automation considerations
- Employee-impacting decision support exposure
- GDPR-sensitive employee data handling
- Explainability and auditability requirements
- Human oversight obligations

---

## Agent Topology

### Agent Layers

| Agent | Responsibilities | Restrictions | Approval Required |
|---|---|---|---|
| Intake Agent | Intent detection, routing, classification | Cannot execute workflows | No |
| Policy Agent | Retrieve and interpret HR policies | Cannot override policy | No |
| Workflow Agent | Generate HR workflow actions | Cannot finalize sensitive actions | Conditional |
| Approval Agent | Validate approval chains and thresholds | Cannot bypass governance | Yes |
| Document Agent | Parse onboarding and HR documents | Cannot finalize employee records | Conditional |
| Governance Agent | Monitor compliance and confidence scoring | Cannot modify workflows directly | No |
| Escalation Agent | Trigger HITL workflows | Cannot make final business decisions | Yes |

### Topology Principles
- Specialized agents over monolithic reasoning
- Shared organizational memory
- Explicit approval boundaries
- Confidence-aware orchestration
- Deterministic governance layer over probabilistic reasoning

### Approval Philosophy
> AI can recommend and orchestrate. Humans remain accountable.

---

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| Unofficial ChatGPT usage for HR policy interpretation | HR Operations | H | govern |
| Spreadsheet-based approval trackers | Regional HR teams | M | replace |
| Manual onboarding email automations | Local HR admins | M | govern |
| Unapproved browser AI extensions | Individual employees | H | kill |
| Personal AI note-taking tools with employee data | Managers | H | govern |
| Legacy workflow macros | Shared services | L | keep |

---

**Total tools found:**  
27

**Tools after triage:**  
11 approved / governed tools

**Estimated hidden spend:**  
$180K–$350K annually in unmanaged tooling, duplicated workflows, and shadow automation inefficiencies
