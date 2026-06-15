# Solution Proposal: AI-assisted Strategy Monitoring

## Recommended Solution
**An AI-supported strategy monitoring layer** that aggregates departmental KPI inputs, detects deviations from strategic targets, and delivers automated early-warning signals to leadership — replacing the annual manual review cycle with continuous visibility.

## What It Is (Precisely)
- A lightweight dashboard that pulls KPI data from existing department inputs (Excel, SharePoint, or simple forms)
- An AI layer (LLM or rule-based) that compares actuals vs. targets and generates plain-language deviation summaries
- A weekly/monthly leadership report generated automatically
- Not: a data warehouse, not a full BI transformation, not an AI decision engine

## Recommendation to Cleo
**Run a 3-month pilot — do not commit to full rollout yet.**

Reasoning:
1. Data readiness is the unknown variable — you cannot assess it without looking inside
2. Change resistance from department heads is predictable — pilot limits exposure
3. Cost of pilot is low (~15-25k€) relative to information value
4. If pilot succeeds: rollout is fast. If it fails: you learn cheaply.

## Pilot Scope
- One department (e.g., Controlling or one strategic program area)
- 3-5 KPIs maximum
- 3 months runtime
- Success metric: leadership spends 50% less time on manual report consolidation

## Build vs. Buy Recommendation
**Buy first, customize later.**
- Start with Perdoo or Power BI + Copilot (existing MS licensing likely)
- Avoid custom build in pilot phase — too slow, too risky
- Custom Python solution only if off-the-shelf tools fail data requirements