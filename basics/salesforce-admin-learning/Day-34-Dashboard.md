# Day 34: Salesforce Dashboards

## What is a Dashboard?

A Salesforce Dashboard is a visual representation of report data.

It helps users quickly understand:
- Key numbers
- Trends
- Comparisons
- Distribution of records

### Report vs Dashboard

Report → Detailed data and analysis  
Dashboard → Visual summary of reports

---

## Dashboard Components

A dashboard can display report data using components such as:

- Charts
- Tables
- Metrics
- Gauges

The available component types depend on the structure of the source report.

---

# Hospital Management Dashboard

Created a dashboard for the Hospital Management System using our existing reports.

### Components Created

### 1. Total Patients

Source Report:
`All Patients Report`

Display:
`Metric`

Purpose:
Shows the total number of patients.

---

### 2. Patients by Department

Source Report:
`Patients by Department`

Display:
`Donut Chart`

Purpose:
Shows how patients are distributed across different departments.

Example:
- Neurology
- Oncology
- Pediatrics
- Pulmonology

---

### 3. Appointments by Status

Source Report:
`Appointments by Status`

Display:
`Bar Chart`

Purpose:
Shows the number of appointments for each status.

Example:
- Scheduled
- Confirmed
- In Progress
- Cancelled

---

### 4. Hospital Billing Summary

Source Report:
`Hospital Billing Summary`

Display:
`Horizontal Bar Chart`

Purpose:
Shows billing amounts for different patients.

This is useful for comparing revenue/billing values.

---

# Important Dashboard Concepts

### Source Report

Every dashboard component gets its data from a Salesforce report.

### Dashboard Component

The visual representation of the report data.

### Dashboard Filter

Allows users to filter dashboard data without changing the underlying reports.

Example:

`Department = Neurology`

### Dynamic Dashboard

A dashboard can be configured to display data based on the running user's access.

This is useful when different users should see different data.

---

# Interview Points

**Q: What is a Salesforce Dashboard?**  
A: A dashboard is a visual summary of Salesforce report data using charts, metrics, tables, and other components.

---
**Q: Can a dashboard exist without a report?**  
A: No. Dashboard components use reports as their data source.

---
**Q: What is the difference between a report and dashboard?**  
A: A report provides detailed data and analysis, while a dashboard presents report data visually for quick decision-making.

---
**Q: Can one report be used in multiple dashboard components?**  
A: Yes, a report can be used as the source for multiple dashboard components.

---
**Q: What is a dashboard filter?**  
A: It allows users to change the data displayed across dashboard components based on selected criteria.

