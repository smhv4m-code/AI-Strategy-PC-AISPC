# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | H | H / M / L | Inventory all critical modules, contracts, renewal dates, support SLAs, and single points of vendor dependence |
| **Abstraction** | M | H / M / L | Map integrations and identify where middleware / API abstraction layer can decouple downstream systems |
| **Routing** | M | H / M / L | Identify top 5 HR workflows that could be rerouted via APIs, service layer, or external portal if needed |
| **Eval** | H | H / M / L | Launch rapid comparison scorecard: cost, UX, AI capability, migration complexity, roadmap risk |

## Portability Score
<!-- Ready / Partial / Locked --> Partial

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? --> Freeze expansions, reduce utilization, Launch competitive benchmark against Workday, Oracle HCM Cloud, niche alternatives

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
If SAP ships a competing product they sunset the existing product and make it mandatory to transition to new product by a certain date, so we will launch the migration/implementation Project
