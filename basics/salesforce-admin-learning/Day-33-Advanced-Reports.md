# Day 37: Advanced Reports in Salesforce

## Advanced Report Features

Salesforce Reports become powerful using:

- Advanced Filters
- Filter Logic
- Relative Date Filters
- Cross Filters
- Grouping & Summaries
- Row-Level Formula
- Summary Formula
- Bucket Fields
- Conditional Highlighting

---

## Advanced Filters

Used to narrow down report records.

Example:

Department = Cardiology

AND

Status = Completed

Filters help show only the records required for a business question.

---

## Filter Logic

Controls how multiple filters are combined.

Example:

1. Department = Cardiology
2. Status = Completed

Filter Logic:

1 AND 2

Can also use OR when either condition should match.

---

## Relative Date Filters

Used to create dynamic date-based reports.

Examples:

- TODAY
- THIS MONTH
- LAST MONTH
- LAST 30 DAYS

Example:

Appointment Date = TODAY

The report automatically updates as the date changes.

---

## Cross Filters

Used to find records with or without related records.

Example:

Patients WITH Appointments

or

Patients WITHOUT Appointments

Useful for identifying records that have missing related data.

---

## Grouping & Summary

Grouping organizes records into categories.

Example:

Cardiology     10
Neurology       7
Orthopedics     5

Summary calculations include:

- SUM
- AVERAGE
- MIN
- MAX

Example:

Total Billing = SUM of Billing Amount

---

## Row-Level Formula

Calculates a value for each individual report row.

Example:

Total = Fee + Tax

Useful when a calculation is required for every record.

---

## Summary Formula

Calculates custom values for grouped report data.

Example:

Confirmed Appointment %

Useful for:

- Percentages
- Performance metrics
- Revenue calculations

---

## Bucket Fields

Categorize report data without creating a new Salesforce field.

Example:

Age

12 → Child
25 → Adult
65 → Senior

Bucket Fields are useful for quickly grouping values into meaningful categories.

---

## Conditional Highlighting

Highlights summary values visually based on conditions.

Example:

0–10 = Low
11–20 = Medium
21+ = High

Useful for quickly identifying important values.

---

## Key Takeaways

- Filters control which records appear.
- Filter Logic combines multiple conditions.
- Relative Date Filters create dynamic date-based reports.
- Cross Filters find records with or without related records.
- Grouping organizes records for analysis.
- Summary functions calculate totals and averages.
- Row-Level Formula works on individual rows.
- Summary Formula calculates custom grouped metrics.
- Bucket Fields categorize data without creating fields.
- Conditional Highlighting improves report visualization.

---

## Interview Questions

### Q1. What is a Cross Filter?

**Answer:**

A Cross Filter allows us to filter records based on whether related records exist or do not exist.

### Q2. What is a Bucket Field?

**Answer:**

A Bucket Field categorizes report values without creating a new field on the Salesforce object.

### Q3. Difference between Row-Level Formula and Summary Formula?

**Answer:**

Row-Level Formula calculates values for individual records, while Summary Formula calculates values based on grouped report data.

### Q4. What are Relative Date Filters?

**Answer:**

They are dynamic date filters such as TODAY, THIS MONTH, and LAST 30 DAYS that automatically update over time.

### Q5. Why are Advanced Reports important?

**Answer:**

Advanced Reports help users analyze Salesforce data, identify business trends, and make better decisions without manually processing records.
