# 3-1-1 Service Requests Dashboard (2025)

## Project Overview
This project analyzes municipal 3-1-1 service requests using an end-to-end data analytics workflow.
The goal is to evaluate operational performance, identify bottlenecks, and present actionable insights through an interactive Power BI dashboard.

The analysis focuses on **2025 data** to provide timely and relevant insights.

---

## Key Questions Answered
- How many service requests were submitted and resolved?
- What percentage of requests remain open (backlog)?
- How quickly are requests typically resolved?
- Which departments have higher resolution times?
- How does workload vary by month?

---

## Key KPIs
- **Total Requests**
- **Closed Requests**
- **Backlog Percentage**
- **Median Resolution Time (Days)**

---

## Dashboard Features
- Interactive KPI cards
- Department-level performance comparison
- Monthly trend analysis
- User-controlled slicers:
  - Department
  - Request Status (Open / Closed)
  - Service Request Type
  - Month (Request Opened)

---

## Data Preparation
Data preparation and KPI engineering were performed in Python using Pandas.

Key steps included:
- Parsing datetime columns
- Handling missing close dates
- Calculating resolution time in days
- Addressing invalid negative resolution values
- Creating analysis-ready fields for Power BI

All data preparation steps are documented in the Jupyter notebook.

📓 Notebook: `notebooks/01_data_cleaning_and_kpis.ipynb`

---

## Technology Stack
- **Python** (Pandas, Jupyter Notebook)
- **Power BI**
- **DAX**
- **GitHub**

---


## Project Structure

```text
311-service-requests-dashboard/
├── data/
│   └── 3-1-1-service-requests.csv
│
├── notebooks/
│   └── 01_data_cleaning_and_kpis.ipynb
│
├── powerbi/
│   └── 311_dashboard.pbix
│
├── README.md
```
## Key Design Decisions
- Backlog percentage is calculated relative to total workload to avoid misleading results when filtering by request status.
- Status values were transformed from boolean values to semantic labels (Open / Closed) for improved usability.
- Monthly analysis was prioritized over yearly analysis due to the dataset scope.

---

## Outcome
The dashboard provides a clear view of operational efficiency while allowing stakeholders to explore trends, compare departments, and monitor backlog behavior through interactive controls.

---

## Author
Haleh Bozorgnia  
Junior Data Analyst  
Tools: Python | SQL | Power BI | Data Visualization
