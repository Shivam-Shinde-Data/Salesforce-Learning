# Day 18: Master-Detail Relationships

## Introduction

Master-Detail Relationship creates a strong parent-child relationship between Salesforce objects.

In Master-Detail, the child object depends completely on the parent object.

---

# What is Master-Detail Relationship?

Master-Detail is a relationship where:

- Child depends on Parent
- Parent controls security
- Deleting parent deletes child records

---

# Relationship Structure

```text
Master Object
     ↓
Detail Object
```

---

# Key Features

## 1. Strong Relationship

Child records cannot exist without Parent records.

---

## 2. Parent Controls Security

Child object inherits security from Parent object.

---

## 3. Cascade Delete

Deleting parent automatically deletes related child records.

---

## 4. Roll-Up Summary Support

Master-Detail supports Roll-Up Summary Fields.

Roll-Up Summary can calculate:

- Count
- Sum
- Average
- Maximum
- Minimum

from child records.

---

# Lookup vs Master-Detail

| Feature | Lookup | Master-Detail |
|---|---|---|
| Relationship Strength | Loose | Strong |
| Child Independent | Yes | No |
| Parent Controls Security | No | Yes |
| Cascade Delete | No | Yes |
| Roll-Up Summary Support | No | Yes |

---

# Real-World Examples

| Parent | Child |
|---|---|
| Order | Order Items |
| Invoice | Invoice Lines |
| Opportunity | Opportunity Products |

---

# Why Lookup Was Used Earlier

Lookup was used in Student Management System because Students should remain independent even if Courses are deleted.

---

# Key Takeaways

- Master-Detail creates strong parent-child relationships.
- Child records depend on Parent records.
- Parent controls child security.
- Cascade Delete automatically removes child records.
- Roll-Up Summary Fields work only with Master-Detail.

