# 3-1-1 Service Requests Dashboard (2025)

![Dashboard Preview](screenshots/dashboard_preview.png)

## Project Overview

This project analyzes municipal **3-1-1 service requests** using an end-to-end data analytics workflow. The objective is to assess operational performance, identify service bottlenecks, and deliver **actionable insights** through an interactive **Power BI dashboard** designed for operational monitoring.

The analysis focuses on **2025 service request data** to provide timely and operationally relevant insights for municipal decision-makers.

---

## Key Business Questions

- How many service requests were submitted and resolved?
- What proportion of requests remains open (**backlog**)?
- How long does it typically take to resolve a request?
- Which departments experience longer resolution times?
- How does service demand fluctuate by month?

---

## Key KPIs

- **Total Service Requests**
- **Closed Requests**
- **Open Requests**
- **Backlog Percentage (~3.6%)**
- **Median Resolution Time (Days)**
- **Average Resolution Time (Days)**

Median resolution time is used as the **primary performance metric** to reduce the influence of long-tail outliers, ensuring a more representative view of typical service delivery. Reporting both median and average resolution times provides additional context on variability and extreme cases.

---

## Dashboard Features

- KPI cards summarizing overall workload and backlog
- Monthly trend analysis of service request volume
- Department-level comparison of median resolution times
- Request status breakdown (Open vs Closed)
- Interactive slicers for:
  - Department
  - Request Status
  - Service Request Type
  - Month

---

## Data Preparation

Data preparation and KPI engineering were performed in **Python (Pandas)** to ensure clean, analysis-ready inputs for Power BI.

Key steps included:
- Parsing and standardizing datetime fields
- Handling missing request close dates
- Calculating resolution time in days
- Identifying and correcting invalid negative resolution values
- Creating Power BI–ready analytical fields and metrics

📓 **Notebook:** `notebooks/01_data_cleaning_and_kpis.ipynb`

---

## Operational Use & Potential Impact

While this project analyzes historical 3-1-1 service data, the dashboard is designed to support operational decision-making by:

- Providing early visibility into backlog levels and resolution delays
- Highlighting departments with consistently longer median resolution times for targeted review
- Supporting resource allocation discussions using monthly demand and resolution trends
- Enabling ongoing performance monitoring if refreshed with new data

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
├── screenshots/
│   └── dashboard_preview.png
│
├── README.md
```
