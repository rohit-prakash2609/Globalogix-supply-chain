
# 🧠 GlobalLogiX | Supply Chain Dashboard (Power BI)

This repository showcases an enterprise-grade Power BI solution developed for **GlobalLogiX**, a multinational logistics company. The project is based on a real-world case study to assess and mitigate supply chain risks using advanced data modeling, DAX, and interactive dashboards.

---

## 🗂️ Project Overview

As part of a skill assessment, this solution delivers strategic insights across procurement, shipments, inventory, supplier risk, and return metrics. It transforms five raw datasets into a unified semantic model and builds drillable visual stories for decision-makers.

### 📌 Business Context
GlobalLogiX operates complex logistics across geographies, facing increasing risk from:

- Unreliable suppliers
- Shipment delays and damages
- Inefficient warehousing
- High return costs

---

## 📊 Key Dashboards & Use Cases

### 🔰 Beginner Scenarios
- **📉 High-Risk Suppliers**  
  Filters suppliers with `Risk Score > 80` and `Reliability < 3`. Tabular format with conditional flags.

- **📈 Delayed Shipments Trend (Last 6 Months)**  
  Monthly line chart of late deliveries to monitor service degradation.

- **📦 Inventory Health by Warehouse**  
  Bar chart highlighting low-stock warehouses with dynamic thresholds.

---

### ⚙ Intermediate Scenarios
- **🔁 Return Reasons Distribution**  
  Pie chart showing percentage breakdown of top return causes.

- **🚚 On-Time vs Delayed Deliveries by Region**  
  Stacked bar chart comparing regional delivery performance.

- **🎯 Supplier Performance Dashboard**  
  Visual drill-down into supplier metrics: delivery punctuality, risk index, and defect rates.

- **📌 KPI Tiles**  
  - % Late Shipments  
  - Avg. Delivery Time  
  - Avg. Supplier Risk

- **📊 Demand Forecasting**  
  Predictive line chart using historical order data (Quarterly Forecast).

---

### 🔬 Advanced Scenario
- **🔥 Composite Supply Chain Risk Score**  
  A weighted model combining:
  - Supplier Risk Score (40%)  
  - Shipment Delay Frequency (30%)  
  - Product Defect Rate (20%)  
  - Inventory Shortages (10%)  
  Output visualized via regional heatmap.

---

## 🛠️ Tech Stack

| Component          | Used For                           |
|--------------------|------------------------------------|
| Power BI Desktop   | Report building and modeling       |
| DAX                | KPIs, risk scoring, time intelligence |
| Power Query (M)    | Data cleaning and transformation   |
| Excel              | Structured source data             |

---

## 🧪 Data Model & Cleaning

> Data was cleaned and segmented into 5 structured tables:

- **Orders.xlsx**
- **Returns.xlsx**
- **Shipments.xlsx**
- **Suppliers.xlsx**
- **Warehouses.xlsx**

Each dataset was modeled with normalized relationships. Redundant columns were removed, calculated columns and hierarchies added.

---

## 🧠 Corrected Logical Errors

### ❌ Flawed DAX Formula:
```DAX
LateShipmentPct = COUNTROWS(Shipments[Status] = "Delayed") / COUNTROWS(Shipments)
```

### ✅ Fixed DAX:
```DAX
LateShipmentPct = 
DIVIDE(
    CALCULATE(COUNTROWS(Shipments), Shipments[Status] = "Delayed"),
    COUNTROWS(Shipments)
)
```

### ❌ Wrong Relationship:
Orders ↔ Shipments via WarehouseID

### ✅ Corrected:
Orders ↔ Shipments via **OrderID**

---

## 📁 Included Files

| File                          | Description                                       |
|-------------------------------|---------------------------------------------------|
| `Rohit_Prakash_CPDA_B2.pbix`  | Final Power BI dashboard (interactive & clean)    |
| `Supply_Chain_Data.xlsx`      | Cleaned data tables (5 sheets)                    |
| `Power BI Skill Test.pdf`     | Official case study prompt from GlobalLogiX       |

---

## 🧑‍💼 Author

**Rohit Prakash**  
📍 Power BI Analyst | Data-Driven Problem Solver   
🧾 Portfolio Projects: Inventory Management, Sales Forecasting, KPI Dashboards

---

![image](https://github.com/user-attachments/assets/a6993b17-9d65-42f1-86bc-c93c50ab15ec)

![image](https://github.com/user-attachments/assets/709868a4-9314-4721-974a-9e5f8b46fa52)
