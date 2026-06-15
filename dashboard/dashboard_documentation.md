# Dashboard Documentation

## Overview

| Item | Detail |
|---|---|
| **File** | `dashboard_dena_en.html` |
| **Tool** | HTML + Plotly.js (standalone, no server required) |
| **Dataset** | IBM HR Analytics Employee Attrition (processed) |
| **Audience** | Cleo, CEO — non-technical stakeholder |
| **Purpose** | Communication layer: evidence for AI adoption investment decision |

---

## Design Principles Applied

**Communication layer, not analysis layer.**
The dashboard is built for a CEO making an investment decision — not for an analyst exploring data. Every chart answers one question Cleo would ask.

**Stakeholder-focused metric selection.**
Metrics were chosen for business relevance, not statistical interest. The readiness score and hype table are the centrepiece — not the raw attrition charts.

**Single source of truth.**
All data traces back to one dataset (IBM HR Analytics) plus explicitly cited market reports. No metrics are presented without a source label.

---

## Layout & Sections

### 1. Header / Hero
- Business question stated explicitly upfront
- Pilot readiness score (2.8/5) and investment figure (€19–31k) visible immediately
- Forces Cleo to engage with the decision framing before seeing charts

### 2. KPI Strip (4 metrics)
| Metric | Business Question Answered |
|---|---|
| Overall attrition rate (16.1%) | How unstable is the org baseline? |
| Overtime → attrition risk (3×) | What drives instability most? |
| Critical tenure window (0–2 yrs) | When is risk highest? |
| Training effect (−18pp) | What is the strongest lever? |

### 3. Charts (5 visualisations)
| Chart | Type | Insight |
|---|---|---|
| Attrition by Department | Bar | Variance across units = strategy execution gap |
| Attrition by Tenure | Line + fill | Early warning: new employees highest risk |
| Overtime vs. Attrition | Bar | 3× risk multiplier — workload as change signal |
| Training vs. Attrition | Colour-coded bar | Investment in people reduces attrition 3:1 |
| Market Benchmark | Horizontal bar | Public sector AI adoption growing — window open |

### 4. Hype vs. Evidence Table
Six vendor/media claims assessed against data sources.
Each verdict: ✓ Supported / ⚠ Partial or Overhyped / ✗ False.
Purpose: helps Cleo distinguish real signals from noise before committing budget.

### 5. AI Adoption Readiness Grid
Six dimensions scored 1–5 with colour-coded bars.
Overall: 2.8/5 — pilot-ready, not rollout-ready.
Anchors the recommendation in structured evidence, not opinion.

### 6. Recommendation Block (full-width, dena blue)
Three columns: Recommendation, Pilot Scope, Real Risk.
Designed as the visual conclusion — the action Cleo should take after reading the dashboard.

---

## Design System

| Element | Value |
|---|---|
| Primary blue | `#1200FF` (dena brand) |
| Orange | `#F4621F` (dena brand) |
| Red / alert | `#D93B2B` |
| Green / positive | `#00873F` |
| Background | `#F3F2FA` (lavender) |
| Font | Space Grotesk (matches dena typography) |
| Border gradient | Blue → Orange → Red (dena topbar) |

---

## Data Source & Limitations

**Dataset:** IBM HR Analytics Employee Attrition (Kaggle)
`kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset`

**Usage:** Structural analog for organisational performance variance in transformation contexts. Not direct evidence from German public sector organisations.

**Documented limitations:**
- Dataset is US-based and synthetic
- No publicly available German federal agency KPI dataset exists
- Market benchmarks (Gartner, Deloitte, Hamburg pilot) are indicative — not independently verified RCT evidence
- Vendor cost estimates are order-of-magnitude only

These limitations are disclosed in the dashboard footer and in `research/market_research.md`.

---

## How to Open

No server required. Open `dashboard_dena_en.html` directly in any modern browser.
Plotly.js is loaded via CDN — internet connection required for first load.
