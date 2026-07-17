# Enterprise Spend Intelligence Dashboard — Finance & Cost Centre Analytics

A Power BI portfolio project simulating a GCC (Global Capability Centre) finance analytics use case — tracking budget vs. actual spend across departments, cost centres, and vendors, with automated variance tiering and corrective action tracking.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-40%2B%20Measures-blue)
![Status](https://img.shields.io/badge/status-complete-brightgreen)

## 🎯 Business Problem

Finance and cost-centre teams need to know **where spend is deviating from budget, how severe the deviation is, and which vendors are driving it** — without manually reconciling spreadsheets across departments and years. This dashboard answers three questions a GCC finance analyst is typically asked:

1. Where is actual spend outpacing budget, and by how much?
2. Which cost categories / departments / vendors are the biggest risk drivers?
3. What corrective action has been taken, and is it working?

## 📊 Dashboard Pages

| Page | Purpose |
|---|---|
| **Home Page** | Landing page with navigation to all views |
| **Vendor Overview** | Budget vs. actual trend by year, variance distribution by cost category, department & vendor YoY performance tables, bookmark-based analysis views |
| **Vendor Heatmap** | Department × Cost Category variance heatmap for fast visual risk-spotting |
| **Vendor Wise Drillthrough** | Native drillthrough (right-click any vendor) showing vendor-level annual spend, variance by cost category / department / cost centre |

## 🧱 Data Model

- **Star schema** — 6 tables (fact spend table + dimension tables for Vendor, Department, Cost Category, Cost Centre, Date)
- **40+ DAX measures**, including:
  - Budget, Actual, and Variance (₹ and %) at multiple grains
  - **4-tier variance classification system** — categorizes variance severity (e.g., Normal / Watch / Elevated / Critical) to flag risk without manual review
  - CAGR and YoY performance measures
  - Context-aware KPI cards (e.g., *Critical Vendors — Selected Category*, which dynamically recalculates against whatever cost category/department is filtered)

## 🔍 Key Features

- **Native drillthrough** on `Vendor_Name`, filtered from the vendor performance table into a dedicated vendor deep-dive page
- **Department × Cost Category heatmap** for pattern recognition across the org
- **Corrective Action Tracker** — links flagged variance to remediation status
- **Bookmark-driven Analysis View** toggle for guided navigation between By Vendor / By Department cuts

## 🛠️ Tools Used

Power BI Desktop · DAX · Power Query · Star Schema Modeling

## 📌 Design Notes

- KPI cards are intentionally context-sensitive (they recalculate against active slicers/cross-filters) rather than fixed — labeled explicitly to avoid ambiguity for viewers.
- The 4% variance threshold was chosen as a materiality baseline; production use would calibrate this per cost category based on historical volatility.

## 📷 Preview

*(Add 2–3 screenshots here: Vendor Overview page, Heatmap page, Drillthrough page)*

## 📁 Files

- `Project_Dashboard.pbix` — full Power BI file
- `screenshots/` — dashboard preview images

## 🔗 Connect

Built by Arkadeep Kar — [LinkedIn](www.linkedin.com/in/arkadeepkar) · [Portfolio](https://github.com/ArKar-Analyst)
