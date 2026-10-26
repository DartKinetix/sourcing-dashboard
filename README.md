# Sourcing ROI Dashboard

A dashboard that shows whether sourcing money is working: how much is spent on each candidate source, and how many placements and how much revenue each source brings back. It was built with Claude as a dashboard artifact (Oct 2026) on top of the Sourcing Dashboard in Power BI.

## What's in this repo

| File | What it is |
| --- | --- |
| `index.html` | The dashboard page: layout, charts, tables and the calculations behind them. |

## What the dashboard shows

- **Five headline numbers** for whether sourcing spend is paying off
- **What to do next**: recommendations drawn from the numbers (which paid sources to keep, grow or review)
- **Budget vs. results**: each source's share of spend against its share of placements and revenue
- **Source scorecard**: spend, candidates added, placements, revenue and return for each source
- **Database reuse**: how often placements come from people already in the candidate database
- **Client mix**: which clients the paid sourcing supports, and where low-fee clients pull returns down
- **Monthly trends**: spend vs. revenue, cost per placement, revenue per placement and return per $1
- **Data health**: candidates added with no usable source, by fiscal month
- **How the numbers are worked out**: definitions for each metric

Reporting uses fiscal months, which start on a Monday and run 4, 4, then 5 weeks.

## Data is not included

The data comes from the Sourcing Dashboard in Power BI (spend by source, candidates added, placements, revenue and client mix). It is **not included in this repository**, because it contains client names and revenue.

`index.html` reads its numbers from named data sources (`source_month`, `scorecard`, `clients`, `cohort_rates`, `spend_years` and similar), so opening the file by itself will not show charts. It needs to run inside the Claude dashboard environment, where those sources are attached, or be adapted to read data you provide.

## Metric definitions

The page includes a "How these numbers are worked out" section that defines each metric, for example return per $1: placement revenue from paid sources divided by what they cost.
