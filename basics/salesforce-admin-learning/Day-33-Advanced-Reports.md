# Day 33: Advanced Reports in Salesforce

## Advanced Report Features

Salesforce Reports become powerful using:

- Advanced Filters
- Cross Filters
- Row-Level Formula
- Summary Formula
- Bucket Fields
- Conditional Highlighting

---

# Advanced Filters

Example:

```text
Department = Cardiology

AND

Status = Completed
```

Filters help narrow down records.

---

# Cross Filters

Used to find:

```text
Records WITH related records

OR

Records WITHOUT related records
```

Example:

```text
Patients WITHOUT Appointments
```

---

# Row-Level Formula

Calculates values for each row.

Example:

```text
Total = Fee + Tax
```

---

# Summary Formula

Calculates values on grouped records.

Example:

```text
Doctor Revenue

Rahul = 3000

Priya = 1500
```

---

# Bucket Fields

Group records without creating fields.

Example:

| Age | Bucket |
|---|---|
| 12 | Child |
| 25 | Adult |
| 65 | Senior |

---

# Conditional Highlighting

Highlights report values visually.

Example:

```text
0-10 = Low

11-20 = Medium

21+ = High
```

---

# Key Takeaways

- Advanced Filters combine multiple conditions.
- Cross Filters show records with or without related records.
- Row-Level Formula works on individual rows.
- Summary Formula works on grouped records.
- Bucket Fields categorize data.
- Conditional Highlighting improves visualization.
