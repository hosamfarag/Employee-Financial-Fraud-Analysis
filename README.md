# Employee-Financial-Fraud-Analysis
An advanced Power BI & DAX project designed to monitor, detect, and evaluate internal financial fraud risks and employee compensation anomalies (Payroll, Overtime, and Bonuses).
# Employee Compensation & Financial Fraud Risk Dashboard 📊🚫

## 📌 Project Overview
This Power BI project is designed to monitor and detect internal financial fraud and anomalies within employee compensation data (Payroll, Bonuses, Overtime). It evaluates employee behaviors through multiple advanced logic checks and flags high-risk individuals using a dynamic **Fraud Score** and **Risk Level** system.

## 🛠️ Tech Stack & Concepts Used
- **Power BI Desktop**
- **DAX (Data Analysis Expressions):** Advanced Calculated Columns, Measures, and Context Transition (`CALCULATE`, `SWITCH`, `SELECTEDVALUE`, `PERCENTILE.INC`).
- **Data Modeling:** Star Schema / Table Relationships.

## 💡 Business Logic & Alerts Created
The **Fraud Score** (Max 100) is calculated dynamically based on 5 weighted metrics:
1. **New Hire High Bonus Alert (Weight: 25):** Flags new hires receiving unusual bonuses (> 3500).
2. **High Salary Low Rating (Weight: 35):** Flags employees in the top 90th percentile of salaries but with a performance rating below 3.
3. **Promotion Alert (Weight: 20):** Flags employees marked eligible for promotion despite low performance ratings (< 3).
4. **New Hire High Salary (Weight: 10):** Flags newly hired employees with salaries exceeding 50,000.
5. **Overtime Alert (Weight: 10):** Flags employees whose overtime hours exceed the 95th percentile of the company.

### Risk Level Segmentation:
- **>= 60:** High Suspicious 🔴
- **>= 30:** Low Suspicious 🟡
- **Other:** Normal 🟢

## 📸 Dashboard Preview
*Insert a screenshot of your beautiful dashboard here*
`![Dashboard Showcase](Screenshots/Financial Fraud Risk Dashboard.jpg)`

## 🚀 How to Run the Project
1. Clone this repository.
2. Download the `.pbix` file from the `PowerBI-File` folder.
3. Open it using Power BI Desktop.
