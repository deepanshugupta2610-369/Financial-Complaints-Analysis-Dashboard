# 📊 Financial Complaints Overview Dashboard (Power BI)
<br>

## 🧾 Project Summary
<br>
This project delivers an interactive Power BI dashboard that helps a financial institution monitor and analyze **customer complaints** to improve:
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

**Objective:** Build a Power BI dashboard that provides a holistic view of complaint behavior and resolution performance to enable data-driven decision-making. 
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

Dataset was cleaned, standardized, and modeled to enable time intelligence and consistent filtering.
<br>

---

## 🧠 Approach & Methodology
<br>

### 1) Data Understanding & Cleaning
<br>

→ Imported the raw CSV dataset containing **~75K financial complaint records**  
<br>
→ Reviewed dataset structure, column definitions, and missing value patterns  
<br>
→ Fixed incorrect **date formats (DD-MM-YYYY → Date)** to enable accurate time-based analysis  
<br>
→ Standardized key categorical text fields for consistency across reporting:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Product  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Issue  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Company Response  
<br>
→ Improved data quality by handling:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Duplicate records  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Null / blank values  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Inconsistent category labels  
<br>
→ Created a dedicated **Date Table** to support time intelligence such as:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Monthly trends  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Seasonality tracking  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Year-over-Year (YoY) comparison  
<br>

### 2) Data Modelling
<br>

→ Implemented a clean **Star Schema** model to improve analytical performance and scalability  
<br>
→ Designed tables as:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ **Fact Table:** Financial Complaints  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ **Dimension Table:** Date Table  
<br>
→ Built relationship for accurate filtering:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ **One-to-many mapping:** Date Table[Date] → Complaints[Date Received]  
<br>
→ Ensured model reliability and dashboard efficiency through:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Clean filter propagation  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Accurate slicing across visuals  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Optimized performance for interactive dashboarding  
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
  <br>
  Date intelligence using Date Table
- `DATEADD`
- `FILTER`
<br>


### 4) Visualization & Storytelling (Dashboard Build)
<br>

→ Designed the dashboard using a **leadership-first layout**: KPIs → Drivers → Deep dive insights  
<br>
→ Built interactive visuals to answer key business questions:  
<br>
<br>
→ **KPI Cards (Executive Summary):**  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Total complaints  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Timely response %  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Disputed rate %  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Resolved at no cost %  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ In-progress complaint count  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ YoY complaint change %  
<br>
<br>
→ **Trend Analysis (Line Chart):**  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Monthly complaint trend for seasonality + spike detection  
<br>
<br>
→ **Issue Driver Analysis (Bar Chart):**  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Identifies top complaint issues to prioritize operational fixes  
<br>
<br>
→ **Geographic Hotspot Analysis (Map):**  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ State-wise complaint concentration for regional investigation  
<br>
<br>
→ **Product Distribution (Treemap):**  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Highlights product categories driving the highest complaint volume  
<br>
<br>
→ **Dispute Composition (Donut Chart):**  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Disputed vs Non-disputed complaint breakdown  
<br>
<br>
→ Added slicers for complaint channel segmentation:  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Email  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Fax  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Phone  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Postal Mail  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Referral  
<br>
&nbsp;&nbsp;&nbsp;&nbsp;→ Web  
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

<br>

## **📌 Strategic Recommendations for Risk & Product Leaders**

<br>

### **1) Targeted Training (Support & Ops Enablement)**
- Focus frontline training on the **top complaint-driving issues** to reduce recurring service gaps.
- Prioritize process reinforcement for:
  - **Managing Accounts**
  - **Deposits & Withdrawals**
- Goal: Address the **high-frequency drivers (~top 20% issues)** that contribute to a major share of complaint volume.
- Expected Impact:
  - Faster resolution turnaround
  - Lower repeat complaints
  - Improved customer satisfaction consistency

<br>

### **2) Dispute Investigation (Quality & Resolution Audit)**
- Audit the **~9.7% disputed complaints** to identify resolution quality gaps.
- Investigate whether the “Resolved at No Cost” approach is:
  - Misaligned with customer expectations, or
  - Closing tickets without solving root cause
- Implement:
  - Dispute root-cause categorization
  - Supervisor review for disputed closures
  - Resolution quality checklist
- Expected Impact:
  - Reduced dispute rate
  - Improved trust and resolution credibility
  - Stronger compliance & customer fairness perception

<br>

### **3) Product Review (Credit Cards & UX Improvements)**
- Product leaders should review the **Credit Card complaint category** since it contributes a major share (**~25% of volume**).
- Recommended actions:
  - Review **fees/charges communication clarity**
  - Improve **billing & dispute journey UX**
  - Simplify **T&Cs** and key policy touchpoints
- Expected Impact:
  - Lower product-driven complaint volume
  - Better retention + reduced churn risk
  - Stronger long-term product experience

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

