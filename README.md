# AI Adoption Readiness Dashboard: Public Sector Strategy Monitoring

**Bootcamp:** Ironhack AI Consulting Bootcamp — Project 5  
**Sector:** Public Sector / Federal Agencies  
**Company Size:** Large (200+ employees)  
**Timeline:** Week 8

---

## Business Question

> "Can AI help a federal agency monitor strategy progress continuously — instead of flying blind until the annual review?"

## Use Case Summary

**AI-supported KPI monitoring layer** for federal agencies that:
- Aggregates departmental performance inputs automatically
- Detects deviations from strategic targets in real-time
- Delivers early-warning signals to leadership
- Reduces time-to-insight from annual reviews → monthly dashboards

**Why this use case?**
- Public sector has limited AI adoption (18% vs. 35% in private sector)
- Strategy monitoring is a low-risk, high-ROI starting point
- Employee attrition patterns are a proxy for organizational health signals
- Evidence-backed business case with measurable KPIs

**Stakeholders:**
- Cleo (CEO/decision-maker): Needs data for investment decisions
- Department heads: Need early visibility into performance gaps
- IT/Data teams: Need sustainable, maintainable automation

---

## Quick Start

### Prerequisites
- Python 3.8+
- pip

### Installation

```bash
# Clone or navigate to the repository
cd ai-adoption-opportunity-project

# Create virtual environment
python -m venv venv
source venv/bin/activate  # macOS/Linux
# or
venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt
```

### Run the Dashboard

```bash
streamlit run dashboard/dashboard.py
```

Dashboard will open at: **http://localhost:8501**

---

## Project Structure

```
ai-adoption-opportunity-project/
├── data/
│   ├── raw/
│   │   ├── WA_Fn-UseC_-HR-Employee-Attrition.csv          # Original dataset
│   │   └── hr_attrition_cleaned.csv                        # Processed/cleaned
│   └── processed/                                           # (For future pipelines)
├── research/
│   ├── market_research.md                                  # AI adoption trends, sector analysis
│   ├── opportunities_risks.md                              # Opportunity mapping, risk assessment
│   └── use_case_discovery.md                               # Use case selection & justification
├── dashboard/
│   ├── dashboard.py                                        # Streamlit app (main deliverable)
│   └── dashboard_documentation.md                          # Design rationale, metrics explanation
├── implementation/
│   ├── solution_proposal.md                                # Investment recommendation (invest/wait/pilot)
│   └── implementation_plan.md                              # Step-by-step rollout plan
├── cost_estimation/
│   ├── cost_analysis.md                                    # Pilot + production cost estimates
│   └── timeline_estimate.md                                # Phased timeline breakdown
├── requirements.txt                                        # Python dependencies
├── README.md                                               # This file
└── sources.md                                              # Complete source list for research
```

---

## Key Deliverables

### 1. **Dashboard** ✅
- **File:** `dashboard/dashboard.py`
- **Type:** Python Streamlit app
- **Metrics:** 7 KPIs + 6 visualizations
- **Features:**
  - Real-time data loading from CSV
  - Interactive charts (Plotly)
  - Market benchmark comparisons
  - AI adoption readiness grid
  - Vendor hype-vs-evidence table
  - Investment recommendation block

**View:** Run `streamlit run dashboard/dashboard.py`

### 2. **Market Research** ✅
- **File:** `research/market_research.md`
- **Coverage:**
  - Public sector AI adoption trends (18% vs. 35% private sector)
  - German federal agency case studies
  - Gartner/Deloitte market signals
  - Competitor and vendor examples

### 3. **Opportunity & Risk Mapping** ✅
- **File:** `research/opportunities_risks.md`
- **Coverage:**
  - 3 AI adoption opportunities ranked by impact
  - Operational, financial, data, and adoption risks
  - Hype-vs-evidence analysis (6 vendor claims scored)
  - Assumption validation checklist

### 4. **Solution Proposal** ✅
- **File:** `implementation/solution_proposal.md`
- **Recommendation:** **Pilot-ready (2.8/5)**
  - **Decision:** Launch 6-month controlled pilot
  - **Budget:** €19–31k (platform + training)
  - **Success KPI:** 5–8pp attrition reduction within 12 months

### 5. **Implementation Plan** ✅
- **File:** `implementation/implementation_plan.md`
- **Phases:**
  1. Discovery & stakeholder validation (2–3 weeks)
  2. Data access & preparation (2–4 weeks)
  3. Prototype / proof-of-concept (4–6 weeks)
  4. Pilot (6 months)
  5. Rollout & training (if successful)

### 6. **Use Case Discovery** ✅
- **File:** `research/use_case_discovery.md`
- **Process:**
  - Why public sector?
  - Why strategy monitoring as starting point?
  - Dataset justification (proxy for organizational health)
  - Limitations and assumptions documented

---

## Data Source

**Dataset:** IBM HR Analytics Employee Attrition  
**Source:** [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)  
**Size:** 1,470 rows × 34 columns  
**Use:** Structural analog for organizational performance variance in transformation contexts

### Data Limitations
- Dataset is US-based and synthetic (not real German federal data)
- No publicly available German federal agency KPI dataset exists
- Used as proxy to develop methodology; real pilot would use actual organizational data
- See `research/use_case_discovery.md` for detailed assessment

### Data Processing
- Original file: `data/raw/WA_Fn-UseC_-HR-Employee-Attrition.csv`
- Processed file: `data/raw/hr_attrition_cleaned.csv`
- Cleaning steps: Removed rows with missing tenure labels, standardized category encoding
- **Note:** Full cleaning script to be added to `data/` directory

---

## Key Metrics Explained

| Metric | Definition | Business Impact |
|---|---|---|
| **Overall Attrition Rate** | % employees leaving per year | Baseline org stability; 16.1% = above industry avg |
| **Overtime Risk Multiplier** | Attrition rate (overtime=Yes) / (overtime=No) | Workload is strongest single driver (3.0× impact) |
| **Early Career Attrition** | % of 0–2 year employees leaving | Critical window for onboarding failures; 33% loss |
| **Training Effect** | Attrition gap (no training vs. 3+ trainings) | Investment ROI: −18pp reduction in attrition |
| **Market Adoption Rate** | % orgs in sector adopting AI | Public sector at 18% (low); growing window |
| **Readiness Score** | Composite across 6 dimensions | 2.8/5 = pilot-ready, not production-ready |
| **Hype Verdict** | Vendor claims vs. data evidence | Helps Cleo filter signal from noise |

---

## Design Rationale

### Why These Metrics?
- **Communication layer focus:** Every metric answers a question Cleo would ask before investing
- **Business-backed:** Metrics tie directly to operational outcomes (attrition → cost)
- **Evidence-based:** All KPIs sourced from data or cited market reports

### Visualization Choices
- **Bar charts** for departmental variance → highlights execution gaps
- **Line chart** for tenure trends → shows early-career risk window
- **Horizontal bar** for benchmarks → easy comparison
- **Readiness grid** for composite score → structured evidence for "go/no-go" decision

### Design Principles
1. **Clarity > complexity:** Interactive features only where they add insight
2. **Decision-ready:** Layout guides Cleo to recommendation without distraction
3. **Traceable:** Every claim backed by data source or citation
4. **Professional:** dena brand colors (#1200FF, #F4621F) reinforce stakeholder confidence

---

## How to Use the Dashboard

### For Cleo (CEO/Investor)
1. Open dashboard → Read business question and readiness score first
2. Scan KPI strip for headline numbers (attrition rate, training effect)
3. Review charts to understand *why* the recommendation is made
4. Check "Hype vs. Evidence" table to validate vendor claims
5. Review "Recommendation" block at bottom for action items

### For Data Teams
1. Check data source (IBM HR Analytics) and limitations
2. Verify metric calculations in `dashboard.py`
3. Extend dashboard by modifying data paths in `dashboard/dashboard.py`
4. Add real organizational data when available

---

## Technical Stack

- **Language:** Python 3.8+
- **Dashboard Framework:** Streamlit (easy to deploy, no server required)
- **Visualizations:** Plotly (interactive, professional)
- **Data Processing:** Pandas, NumPy
- **Data Storage:** CSV (CSV for simplicity; extend to SQL/cloud for production)

### Why These Tools?
- **Streamlit:** Rapid prototyping, CEO-friendly, no frontend coding
- **Plotly:** Professional-grade charts, exportable to PowerPoint
- **CSV:** Works for pilot; migrate to database for rollout

---

## Deployment

### Local Development
```bash
streamlit run dashboard/dashboard.py
```

### Production Deployment (Future)
Options for scaling:
- **Streamlit Cloud:** Free tier available; easy GitHub integration
- **Docker + AWS/GCP:** For enterprise data pipeline
- **PowerBI / Tableau:** If organization standardizes on these tools

---

## File Guide

| File | Purpose | Status |
|---|---|---|
| `README.md` | Project overview (this file) | ✅ |
| `requirements.txt` | Python dependencies | ✅ |
| `dashboard/dashboard.py` | Streamlit app | ✅ |
| `dashboard/dashboard_documentation.md` | Design & metrics explanation | ✅ |
| `research/market_research.md` | Market trends & adoption signals | ✅ |
| `research/opportunities_risks.md` | Opportunity map, risks, hype analysis | ✅ |
| `research/use_case_discovery.md` | Use case selection & justification | ✅ |
| `implementation/solution_proposal.md` | Investment recommendation | ✅ |
| `implementation/implementation_plan.md` | Step-by-step rollout | ✅ |
| `cost_estimation/cost_analysis.md` | Pilot + production costs | ✅ |
| `cost_estimation/timeline_estimate.md` | Phase timeline | ✅ |
| `sources.md` | Complete source list | ✅ |

---

## Key Findings & Recommendation

### Investment Recommendation: **PILOT** ✅

**Decision:** Launch a 6-month controlled pilot with one high-attrition department (R&D)

**Why?**
- Evidence is pilot-ready: readiness score 2.8/5 (moderate)
- Pilot cost is low: €19–31k (< 0.1% of federal IT budget)
- Risk is contained: Single department + 6-month window
- ROI is measurable: Track attrition reduction, cost savings, adoption rate

**What Would Change the Recommendation?**
- ❌ If data access becomes unavailable → wait for open data initiative (2024–2025)
- ❌ If budget is cut → defer to next fiscal year
- ✅ If pilot shows >8pp attrition improvement → approve full rollout

---

## Next Steps

### For Users
1. Run the dashboard locally
2. Review market research findings
3. Share recommendation with stakeholders
4. Plan pilot kickoff

### For Developers
1. Extend dashboard with real organizational data when available
2. Add data pipeline (currently manual CSV; automate with SQL/API)
3. Build alert system for deviation detection
4. Plan PowerBI/Tableau migration for enterprise scale

---

## Questions?

See detailed documentation in:
- **Market research:** `research/market_research.md`
- **Risks & opportunities:** `research/opportunities_risks.md`
- **Implementation steps:** `implementation/implementation_plan.md`
- **Dashboard design:** `dashboard/dashboard_documentation.md`

---

## Submission Checklist

- [x] GitHub repository with all code and documentation
- [x] README.md with complete setup instructions
- [x] requirements.txt with all dependencies
- [x] Python dashboard file (`dashboard/dashboard.py`)
- [x] Dashboard documentation
- [x] Market research and source list
- [x] Opportunity/risk/hype analysis
- [x] Solution proposal with invest/wait/pilot recommendation
- [x] Implementation plan with steps, timeline, costs, risks, and assumptions
- [x] Project documentation (use case, dataset, architecture, methodology)
- [ ] Presentation (to be added if required)
- [x] All files properly named and organized
- [x] Proper folder structure (research/, dashboard/, implementation/, cost_estimation/, data/)

---

**Last Updated:** June 15, 2026  
**Status:** Project 5 Deliverables — Ready for Submission  
**Version:** 1.0
