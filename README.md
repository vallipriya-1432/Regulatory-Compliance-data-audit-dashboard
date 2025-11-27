# Regulatory Compliance Data Audit Dashboard (Power BI)

## 📌 Overview
This project showcases a complete end-to-end **Regulatory Compliance Data Audit Dashboard** built using **Power BI**.  
The goal of this project was to centralize compliance audit information and provide clear visibility into high-risk violations, overdue items, policy-level patterns, and department compliance posture.

The dashboard is designed from the perspective of a **Risk & Compliance Analyst**, focusing on proactive monitoring and actionable reporting.

---

## 🎯 Project Objectives
- Identify **high-risk audit items** requiring immediate action.
- Track **overdue audits**, recurring issues, and aging trends.
- Provide leadership with **clear, visual insights** for decision-making.
- Highlight **policy areas** with repeated violations or increased risk.
- Centralize audit logs into a clean, interactive data model.

---

## 📂 Dataset
The dataset contains realistic, simulated audit logs with the following fields:

| Column Name     | Description |
|-----------------|-------------|
| Audit_ID        | Unique audit reference number |
| Department      | Business department audited |
| Policy_Area     | Policy or domain area reviewed |
| Risk_Severity   | Risk rating (Low, Medium, High) |
| Audit_Date      | Date of the audit |
| Status          | Open or Closed |
| Findings        | Number of findings discovered |
| Days_Overdue    | How long the audit remains overdue (if open) |

Total rows: **120+**


---

## 🖥️ Dashboard Pages & Features

### **Page 1 — Compliance Overview**
- KPI cards for Total Audits, Open Audits, High-Risk Audits, and Avg. Overdue Days  
- Audit Status breakdown (Open vs Closed)  
- Department-wise findings  
- Trend of audits over time  
- Interactive slicers for department, risk severity, and date  

---

### **Page 2 — High-Risk & Overdue Monitoring**
- High-Risk Audit Table (filtered by severity = High)  
- Overdue Trend Line Chart  
- Heatmap (Department × Policy Area based on findings)  
- KPI: Total Overdue Audits  

---

### **Page 3 — Policy Area Compliance Analysis**
- Donut chart of policy areas distribution  
- Policy × Risk × Findings matrix with conditional formatting  
- KPI: Most Violated Policy  
- Compliance Score Gauge (based on findings)  

---

## 🛠️ Tools & Technologies
- **Microsoft Power BI Desktop**
- **DAX** for custom measures
- **Power Query** for data shaping
- **Excel** for dataset storage and structuring

---

## 📊 Key Measures (DAX)
Some core DAX measures used in this project:

'''DAX
Total Audits = COUNTROWS(Audit_Records)

Open Audits =
CALCULATE([Total Audits], Audit_Records[Status] = "Open")

High Risk Audits =
CALCULATE([Total Audits], Audit_Records[Risk_Severity] = "High")

Avg Overdue Days = AVERAGE(Audit_Records[Days_Overdue])

Overdue Audits =
CALCULATE([Total Audits], Audit_Records[Days_Overdue] > 0)
'''

------

**Additional measures were used for:**

Most Violated Policy

Policy compliance score

-----
**✨ What This Project Demonstrates**

Ability to design full BI reporting solutions

Understanding of audit risk, compliance metrics, and policy governance

Ability to create clean, interactive dashboards

Experience building measures, matrices, heatmaps, and KPI summaries

Strong analytical storytelling for executive audiences

-----

**✔️ Final Notes**

This project is built exactly as a real-world compliance dashboard would be.
It demonstrates practical analytics skills and an understanding of how organizations monitor risk.
