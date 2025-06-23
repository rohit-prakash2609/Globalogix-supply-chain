**🚚 GlobalLogiX – Power BI Supply Chain Risk Management Dashboard**
**Candidate: Rohit Prakash**
**Tool Used: Microsoft Power BI**
**Role: Data Analyst | Dashboard Developer**
**Project Type: Skill Test & Capstone Project**
**Client Simulation: GlobalLogiX (Multinational Logistics Firm)**

**🧭 Overview**
This Power BI project was developed as part of a skill evaluation for GlobalLogiX, a logistics and supply chain company seeking improved operational insights. The dashboard provides end-to-end visibility into supplier performance, inventory health, shipment delays, and return diagnostics. It leverages DAX, Power Query, and drill-through reports to drive real-time decision-making.

**🎯 Objectives**
Identify high-risk, low-reliability suppliers

Track delayed vs. on-time shipments over 6 months

Monitor inventory shortages across warehouses

Analyze return reasons and cost implications

Visualize freight and logistics costs

Build dynamic KPIs for supply chain efficiency

Develop a composite risk score model using weighted DAX

**🧹 Data Cleaning & Preparation**
The original Excel dataset (Suppy_Chain_Data.xlsx) included multiple sheets for suppliers, shipments, orders, returns, and warehouse information. The following preprocessing steps were applied:

**✅ Cleaning Steps:**
Standardized column names (e.g., Risk Score → risk_score)

Converted data types:

Dates (Order_Date, Shipment_Date)

Decimals (Delay_Days, Freight_Cost, Risk_Score)

Filled missing values:

Delay_Days filled with 0

Null values in Risk Score and Reliability handled via imputation or removal

Merged tables via:

Order_ID, Supplier_ID, Warehouse_ID relationships

Calculated fields:

DAX
Copy
Edit
Shipment_Date = RELATED(Orders[Order_Date]) + Shipments[Delay_Days]
Stock Status = IF(Stock_Level < Min_Threshold, "Understocked", "Healthy")
Removed duplicates and validated unique IDs

Derived time intelligence columns: Year, Month, Quarter

Formatted currency and percent fields for visuals

**📈 Power BI Dashboard Features**
Module	Description
Supplier Risk View	Table of high-risk suppliers (Risk > 80, Reliability < 3)
Shipment Trends	Line + bar chart of delayed vs. on-time shipments
Inventory Monitor	Conditional formatting to flag understocked warehouses
Return Analysis	Pie chart of top return reasons
Cost Overview	Freight cost trends and total logistics spend
Composite Risk Map	Heatmap of risk score by region using weighted DAX model
Forecasting Section	Predicted demand based on past order trends

**📌 Key KPIs & DAX Measures**
  **Measures**
  Avg Return Cost = AVERAGE(Returns[Cost])

  Avg Delay Days = AVERAGE(Shipments[Delay_Days])

  Avg Freight Cost = AVERAGE(Shipments[Freight_Cost])

  Delayed Shipment % = Delayed Shipments / Total Shipments

  On Time Shipment % = On Time Shipments / Total Shipments

  HighRiskSupplierCount = COUNTROWS(FILTER(...))

  Total Freight Cost = SUM(Shipments[Freight_Cost])

  **Calculated Columns**
  Shipment_Date derived using order date + delay

  Stock Status column to label understocked warehouses

🔢 Composite Risk Score Model (Advanced DAX)
A weighted formula was created to visualize overall supply chain risk:

DAX
Copy
Edit
Composite Risk Score = 
0.4 * Supplier_Risk_Score +
0.3 * Delay_Frequency +
0.2 * Defect_Rate +
0.1 * Inventory_Shortage
📍 This is visualized through a heatmap for region-level risk comparison.

**🧠 Strategic Insights**
18% of suppliers fall into high-risk, low-reliability category

Shipment delays peaked in Q2 across the South-East region

Top 3 return reasons accounted for 70% of all returns

Several warehouses were flagged as understocked repeatedly

North-West region scored highest composite risk in heatmap

**👨‍💼 About the Analyst**
**Rohit Prakash**
**📍 Data Analyst | Power BI Developer | Supply Chain Enthusiast**


![image](https://github.com/user-attachments/assets/a2fcf4e4-530d-4ea2-966e-2d0492e0bda1)

![image](https://github.com/user-attachments/assets/d6125dd7-77dc-4a97-8dfb-6bd8478b310e)
