# Implementation Plan: AI-assisted Strategy Monitoring
## BundesEnergie Agentur (BEA) — Large Public Sector Organization

---

## Overview

| Item | Detail |
|---|---|
| **Use Case** | AI-supported KPI monitoring replacing annual manual reporting cycle |
| **Recommendation** | Run 3-month pilot before committing to rollout |
| **Total Pilot Cost** | €19,000–31,000 |
| **Total Rollout Cost (Year 1)** | €125,000–200,000 |
| **Break-even** | ~12–16 months post-rollout |
| **Decision Point** | After Phase 1 evaluation (Month 5) |

---

## Phase 0: Discovery & Alignment (Weeks 1–4)

### Goal
Determine whether a pilot is viable before spending a euro on tooling.

### Activities
- [ ] KPI inventory: collect all existing KPIs across departments (what is measured, where, by whom, how often)
- [ ] Data source audit: identify where data lives (Excel, SharePoint, ERP, manual reports)
- [ ] Stakeholder mapping: department heads, Controlling lead, IT security officer
- [ ] Tool selection: evaluate Perdoo vs. Power BI Copilot vs. custom Python
- [ ] BSI compliance pre-check: flag data sensitivity, cloud hosting requirements
- [ ] Go/No-Go decision with Cleo

### Owners
| Activity | Owner |
|---|---|
| KPI inventory | Controlling + OE Lead |
| Data audit | IT + Controlling |
| Stakeholder alignment | CEO / OE Lead |
| Tool evaluation | IT + external consultant |
| BSI pre-check | IT Security Officer |

### Success Criteria
- KPI inventory complete for at least 2 departments
- At least 3 KPIs identified that are clean, consistent, and measurable
- Go/No-Go decision documented with rationale

### Risks in this Phase
- Department heads reluctant to share KPI data → mitigate with top-down mandate from Cleo
- IT security blocks cloud tools → mitigate by identifying on-premise fallback option early

---

## Phase 1: Pilot (Months 2–4)

### Goal
Build a working monitoring dashboard for 1 department, 3–5 KPIs, validate with real users.

### Scope
- **Department:** Controlling or one strategic program area (highest data readiness)
- **KPIs:** 3–5 maximum — chosen for cleanliness, not comprehensiveness
- **Tool:** Perdoo (recommended) or Power BI + Copilot if MS licensing already exists
- **Users:** Department head + 2–3 team leads (pilot group only)

### Implementation Steps

**Week 1–2: Setup**
- Tool provisioning and access setup
- Data input template built (manual input acceptable in pilot)
- Baseline: measure current manual reporting time per week

**Week 3–4: First Dashboard Live**
- 3 KPIs visible: actual vs. target, deviation flags
- Department head has access

**Week 5–8: Stabilization**
- Regular data entry rhythm established
- UX adjustments based on feedback
- Mid-pilot check-in: is reporting time dropping?

**Week 9–12: Measurement**
- Final data collection
- Compare manual reporting hours before vs. during pilot
- Qualitative interviews with pilot group

### Success Metrics
| Metric | Target |
|---|---|
| Reporting time reduction | ≥ 50% vs. baseline |
| Dashboard usage | ≥ 2× per week by dept head |
| User satisfaction | ≥ 3.5/5 in feedback survey |
| Data entry reliability | ≥ 90% of weekly inputs on time |

### Risks in this Phase
| Risk | Mitigation |
|---|---|
| Data entry falls behind | Assign single data owner per KPI |
| Department head disengaged | Weekly 15-min touchpoint, Cleo endorsement visible |
| Tool doesn't fit data structure | Python fallback ready by Week 3 |
| GDPR concern raised | Use only aggregated, non-personal KPIs |

---

## Phase 2: Evaluation & Decision (Month 5)

### Three Possible Outcomes

**Go — Expand to rollout**
Criteria: all 3 success metrics met, department head endorses

**Adjust — Revise and re-pilot**
Criteria: mixed results, clear root cause identified
Next step: 4-week adjustment sprint, then re-measure

**Stop — Don't proceed**
Criteria: data quality too poor, change resistance insurmountable
Outcome: document learnings, re-evaluate in 12 months

---

## Phase 3: Rollout (Months 6–18)

### Sequence by Data Readiness — Not All at Once

| Wave | Scope | Timeline |
|---|---|---|
| Wave 1 | Pilot dept + 1 adjacent | Months 6–8 |
| Wave 2 | 3 additional departments | Months 9–12 |
| Wave 3 | Full organization | Months 13–18 |

### Change Management Plan
| Activity | Purpose | Frequency |
|---|---|---|
| CEO update email | Visible leadership commitment | Monthly |
| Dept head peer sessions | Social proof, problem-sharing | Bi-monthly |
| User training | Reduce friction | Per wave |
| Feedback survey | Catch issues early | Quarterly |

### Key Dependencies
- IT sign-off on data integration architecture
- BSI compliance certificate for chosen tool
- Budget approval (separate board decision required)
- Dedicated PM (1.0 FTE for 12 months)
- Department head buy-in before each wave — non-negotiable

---

## Assumptions & Methodology

| Assumption | Confidence | Impact if Wrong |
|---|---|---|
| At least 3 clean KPIs exist in pilot dept | Medium | Pilot delayed 4–6 weeks |
| Perdoo / Power BI passes BSI review | Medium | On-premise fallback, +€20k |
| Dept head cooperates in pilot | High | Pilot fails — needs Cleo mandate |
| Manual reporting ≥4h/week per dept head | Medium | ROI calculation needs revision |
| EU digitization funding available | Low-Medium | Budget gap of €30–50k Year 1 |

### Methodology Notes
- IBM HR Analytics dataset is a **structural analog** — not German public sector data
- Market benchmarks (Gartner, Deloitte) are **indicative**, not RCT-level evidence
- Hamburg pilot data (−35% reporting time) is from a **press release**, unverified
- Cost estimates are **order-of-magnitude** — real procurement costs will differ

---

## Summary Recommendation to Cleo

> **Invest €19–31k in a 3-month pilot. Decide on rollout only after seeing results.**
>
> The technology is ready. The market signal is clear. The unknown is your data.
> A pilot answers the one question no consultant can answer from the outside:
> *"Is our data good enough to make this work?"*
>
> If yes: rollout pays back in 12–16 months.
> If no: you've spent €25k learning something that would have cost €200k to discover mid-rollout.