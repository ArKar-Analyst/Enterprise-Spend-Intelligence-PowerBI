# Enterprise Spend Intelligence Dashboard

**Power BI project analyzing ₹7B+ in enterprise vendor spend** — flags budget overruns, ranks vendor risk, and drills into root cause across departments and cost centres.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-40%2B%20Measures-blue)

## Preview

![Vendor Overview](screenshots/vendor-overview.png)
![Heatmap](screenshots/heatmap.png)

## What it does

A finance/cost-centre team needs to spot budget overruns fast, know which vendors are driving them, and act on it — this dashboard does that in 4 pages instead of a spreadsheet reconciliation.

| Page | What it shows |
|---|---|
| **Vendor Overview** | Budget vs. actual trend, variance by cost category, vendor YoY performance |
| **Vendor Heatmap** | Department × Cost Category variance heatmap — spot risk in one glance |
| **Vendor Drillthrough** | Right-click any vendor → full spend breakdown by category, department, cost centre |

## Highlights

- **Star schema**, 6 tables, **40+ DAX measures**
- **4-tier variance classification** — auto-flags severity instead of manual review
- **Native drillthrough** wired vendor → detail page
- **Context-aware KPIs** — cards recalculate against active filters, explicitly labeled to avoid ambiguity (e.g. *"Critical Vendors — Selected Category"*)

## Stack

Power BI Desktop · DAX · Power Query · Star Schema Modeling

## Files

- `Project Dashboard.pbix` — full report
- `data/` — source data
- `screenshots/` — page previews

---
Arkadeep Kar — [GitHub](https://github.com/ArKar-Analyst)
