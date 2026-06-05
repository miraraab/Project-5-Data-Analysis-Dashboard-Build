# Use Case Discovery

## Sector & Company
- **Sector:** Public Sector / Federal Agency (Bundesagentur)
- **Company Size:** Large (200+ employees)
- **Fictional Company:** "BundesEnergie Agentur" (BEA) — modeled on dena-type organizations
- **Cleo's Role:** CEO, ~300 employees, mission-driven, politically accountable

## Nordstern-Frage
> "Can AI help a federal agency monitor strategy progress continuously — instead of flying blind until the annual review?"

## Pain Point
Large public sector organizations typically:
- Measure strategy execution **once per year** via manual reporting cycles
- Rely on **decentralized, inconsistent KPI reporting** across departments
- Have **no early warning system** when strategic initiatives fall behind
- Spend significant leadership time on **manual report consolidation**

Result: Strategic course corrections happen too late, political accountability is reactive not proactive.

## Chosen Use Case
**AI-assisted Strategy Monitoring Dashboard**

An AI-supported reporting layer that:
1. Aggregates KPI data from department inputs
2. Detects deviations from strategic targets automatically
3. Surfaces early warning signals to leadership
4. Reduces manual reporting effort by ~60%

## Why This Use Case — Why Now
- Public sector digital transformation is accelerating (Digitalstrategie Bundesregierung 2025)
- Strategy monitoring is a low-risk AI entry point: no sensitive citizen data, no high-stakes automation
- ROI is measurable: time saved on reporting, speed of course correction
- Tools exist at accessible price points (no enterprise-scale investment required for pilot)

## What This Use Case Is NOT
- It does not replace strategic decision-making
- It does not automate KPI target-setting
- It does not predict political outcomes

## Stakeholders & Decision Constraints
| Stakeholder | Need | Constraint |
|---|---|---|
| CEO (Cleo) | Clear strategic overview, early warnings | Limited tech budget, political accountability |
| Department Heads | Less reporting burden | Change resistance, data ownership concerns |
| Controlling | Consistent data quality | Legacy systems, no unified data model |
| IT/Data | Maintainable solution | GDPR, BSI compliance requirements |

## Dataset Justification
**IBM HR Analytics Attrition Dataset (Kaggle)**
Used as proxy for organizational performance metrics in transformation contexts.
- Attrition rate → proxy for change resistance / org health during strategy shifts
- Department performance variance → proxy for uneven strategy execution
- Manager satisfaction scores → proxy for leadership effectiveness in driving strategy

*Limitation (documented):* Dataset is US-based and synthetic. Real public sector KPI data is not publicly available in Germany. This analysis uses the dataset as a structural analog, not as direct evidence.