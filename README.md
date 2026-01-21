# 📊 Financial Complaints Overview Dashboard (Power BI)
<br>

## 🧾 Project Summary
<br>
This project delivers an **interactive Power BI dashboard** that helps a financial institution monitor and analyze **customer complaints** to improve:
- Customer experience (CX)
- Operational efficiency
- Complaint resolution performance
- Compliance visibility & regulatory readiness
<br>

The dashboard converts raw complaint records into **decision-ready insights** for:
- Risk teams
- Product owners
- Customer service managers
<br>

---

## 🎯 Business Problem / Objective
<br>
A financial institution receives thousands of customer complaints every year. Leadership needs a consolidated view to:
- Track complaint volume trends
- Measure responsiveness
- Identify top complaint drivers (issues/products)
- Detect geographic hotspots
- Monitor resolution outcomes (disputed/resolved/in-progress)
<br>

**Objective:** Build a Power BI dashboard that provides a holistic view of complaint behavior and resolution performance to enable data-driven decision-making. :contentReference[oaicite:3]{index=3}
<br>

---

## 📌 Key KPIs in Dashboard
<br>

| KPI | Description |
|---|---|
| **Total Complaints** | Overall number of complaints received |
| **Timely Response %** | % complaints responded within acceptable timeframe |
| **Disputed Rate %** | % complaints escalated/disputed by consumers |
| **Resolved at No Cost %** | % cases resolved without monetary compensation |
| **In Progress** | Complaints currently unresolved / being processed |
| **YoY Complaint Change %** | Year-over-year change in complaint volume |

<br>

---

## 🗂 Dataset Overview
<br>

**Dataset:** Financial Consumer Complaints (CSV)  
**Records:** ~75,000 complaint records  
**Date Range (Dashboard):** 01-12-2011 to 13-10-2020  
<br>

**Key Fields Used**
- Date Received
- Issue
- Product
- State
- Consumer Disputed
- Timely Response
- Company Response / Resolution status
<br>

Dataset was cleaned, standardized, and modeled to enable time intelligence and consistent filtering. :contentReference[oaicite:4]{index=4}
<br>

---

## 🧠 Approach & Methodology
<br>

### 1) Data Understanding & Cleaning
<br>

- Imported raw CSV dataset containing **~75K financial complaint records**
<br>
- Reviewed dataset structure, column definitions, and missing value patterns
<br>
- Fixed incorrect **date formats (DD-MM-YYYY → Date)** for accurate time analysis
<br>
- Standardized key categorical text fields for consistency:
  - Product
  - Issue
  - Company Response
<br>
- Removed data quality issues:
  - Duplicate records
  - Null / blank entries
  - Inconsistent category labels
<br>
- Created a dedicated **Date Table** to enable proper time intelligence:
  - Monthly trends
  - Seasonality tracking
  - Year-over-year (YoY) comparison
<br>

### 2) Data Modelling
<br>

- Implemented a clean **Star Schema** model to improve analytical performance
<br>
- Designed tables as:
  - **Fact Table:** Financial Complaints
   <br>
  - **Dimension Table:** Date Table
<br>
- Built relationship:
  - **One-to-many mapping:**
    <br>
  - Date Table[Date] → Complaints[Date Received]
<br>
- Ensured:
  - Clean filter propagation
  - Accurate slicing across visuals
  - Optimized model performance for interactive dashboarding
<br>


### 3) DAX Measures (Metrics Layer)
<br>
Key DAX measures created:
- Total Complaints
- Timely Response %
- Disputed Rate %
- Resolved at No Cost %
- In-Progress Complaints
- YOY Complaint Change %
<br>

Common DAX patterns used:
- `CALCULATE`
- `SUM`
- `DIVIDE`
- Date intelligence using Date Table
- `DATEADD`
- `FILTER`
<br>
(Confirmed in project summary PDF.) :contentReference[oaicite:7]{index=7}
<br>

### 4) Visualization & Storytelling
<br>
Visual components included:
- KPI Cards (executive summary layer)
- Monthly trend chart (seasonality tracking)
- Complaints by Issue (bar chart)
- Complaints by State (US map / hotspot analysis)
- Complaints by Product (tree map / distribution)
- Consumer Disputed % (donut chart)
- Interactive slicers by channels:
  - Email
  - Fax
  - Phone
  - Postal Mail
  - Referral
  - Web
<br>
(As per dashboard visuals list.) :contentReference[oaicite:8]{index=8}
<br>

---

## 🧩 Dashboard Features (What Business Can Answer)
<br>

✅ Leadership can instantly answer:
- Are complaints rising or falling YoY?
- Which issues generate the most complaints?
- Which products are risk-heavy in customer dissatisfaction?
- Which states show higher complaint concentration?
- Are we responding on time?
- Are customers disputing resolutions despite timely response?
- How many complaints are still open / in progress?
<br>

---

## 🔎 Key Insights (Findings)
<br>

Based on the dashboard analysis:
<br>

### 📈 Complaint Trend & Growth
- Complaint volume increased **YoY by ~14.33%**
- Indicates growing dissatisfaction OR increased service usage / reporting frequency
<br>

### ⏱ Timely Response vs Dispute Gap (Quality issue)
- **98.05%** complaints received timely response
- But **9.71%** cases were disputed by consumers  
✅ This implies: **SLA met ≠ Resolution quality / fairness**
<br>

### 💸 Resolution Efficiency
- **84.50%** complaints were resolved at **no cost**
- Suggests strong non-monetary resolution effectiveness
<br>

### 🧾 Issue-Level Pain Points (Top Drivers)
Highest complaint contributors:
- **Managing an account (~8.8K)**
- **Deposits & withdrawals (~6.1K)**
- Trouble during payment process (~3.5K)
- Struggling to pay mortgage (~3.4K)
- Problem with purchase shown on statement (~3.3K)
- Billing disputes (~3.2K)
<br>

Managing Accounts + Deposits/Withdrawals alone contribute **~20%** of complaints.
<br>

### 🧨 Product Risk Concentration
Top product concentration:
- **Credit card ~25.30%**
- **Checking/Savings account ~17.85%**
Combined: **~43%** complaint concentration
<br>

### 🌍 Geographic Hotspots
- Certain states show disproportionate complaints
- Indicates potential operational inefficiencies, vendor/service gaps, or region-specific customer experience issues
<br>

(All insights are derived from dashboard insight pages.) :contentReference[oaicite:9]{index=9}
<br>

---

## 🏢 Business Impact (Why this matters)
<br>

This dashboard enables leadership to:
- Detect high-risk complaint categories early
- Improve complaint resolution workflows
- Reduce customer dissatisfaction
- Strengthen compliance visibility
- Prioritize product/process improvements backed by data
<br>

---

## ✅ Recommendations (Actionable Next Steps)
<br>

### Quick Wins (0–30 days)
- Identify top 3 complaint issues and create SOPs for resolution
- Improve customer communication templates to reduce disputes
- Weekly monitoring dashboard review with CX & Ops
<br>

### Operational Improvements (30–90 days)
- Segment disputes by:
  - issue
  - product
  - state
- Root cause mapping for top complaint areas:
  - account management
  - deposits/withdrawals
- Establish KPI targets (reduce disputed %)
<br>


## 🛠 Tools & Tech Stack
<br>

- **Power BI Desktop**
- **DAX**
- **Power Query**
- CSV Dataset
<br>

<br>

This project successfully transforms raw financial complaint data into an executive-ready analytics dashboard, helping stakeholders across Risk, Product, and Customer Service teams to align on:

- Complaint drivers

- Resolution performance

- Customer dispute behavior

- Operational risk hotspots

