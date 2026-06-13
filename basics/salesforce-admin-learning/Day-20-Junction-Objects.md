# Day 24: Junction Objects

## Introduction

Junction Objects are used in Salesforce to create Many-to-Many Relationships between objects.

A Junction Object acts as a bridge between two objects.

---

# What is Many-to-Many Relationship?

Many-to-Many means:

- One record can connect to many records
- On both sides of the relationship

Example:

- One Student can join many Courses
- One Course can contain many Students

---

# What is a Junction Object?

A Junction Object is a custom object that connects two objects using two Master-Detail Relationships.

It acts as a bridge object.

---

# Example

```text
Student
   ↓
Enrollment
   ↑
Course
```

Here:

- Student = Parent
- Course = Parent
- Enrollment = Junction Object

---

# Why Junction Objects Are Needed

Salesforce cannot directly create Many-to-Many relationships.

Junction Objects solve this problem.

---

# Junction Object Structure

A Junction Object contains:

- Master-Detail Relationship to Object 1
- Master-Detail Relationship to Object 2

---

# Real-World Examples

| Object 1 | Junction Object | Object 2 |
|---|---|---|
| Student | Enrollment | Course |
| Employee | Assignment | Project |
| Doctor | Appointment | Patient |

---

# Additional Information Storage

Junction Objects can store extra business information.

Example:

Enrollment object can store:

- Enrollment Date
- Fees Paid
- Attendance

---

# Why Master-Detail Relationships Are Used

Master-Detail Relationships provide:

- Strong dependency
- Security inheritance
- Cascade Delete
- Roll-Up Summary support

---

# Key Takeaways

- Junction Objects create Many-to-Many relationships.
- They act as bridge objects.
- Junction Objects use two Master-Detail Relationships.
- They support complex business systems.
- They can store additional business information.

