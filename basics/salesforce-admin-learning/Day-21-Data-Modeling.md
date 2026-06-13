# Day 25: Data Modeling Scenario – College Management System

## Introduction

Data Modeling is the process of designing how business data is stored and connected inside Salesforce.

It is one of the most important Salesforce Admin and Architect skills.

---

# What is Data Modeling?

Data Modeling means planning:

- Objects
- Fields
- Relationships

inside a Salesforce application.

---

# College Management System Objects

| Business Entity | Salesforce Object |
|---|---|
| Student | Student__c |
| Course | Course__c |
| Faculty | Faculty__c |
| Department | Department__c |
| Enrollment | Enrollment__c |
| Fees | Fees__c |

---

# Relationships

## Department → Course

One Department can contain many Courses.

Possible relationship:

- Master-Detail

---

## Faculty → Department

One Department can contain many Faculty members.

Possible relationship:

- Lookup Relationship

---

## Student ↔ Course

One Student can join many Courses.

One Course can contain many Students.

This becomes a Many-to-Many relationship.

Solution:

- Junction Object

---

# Enrollment Object

Enrollment__c acts as Junction Object.

Structure:

```text
Student
   ↓
Enrollment
   ↑
Course
```

Enrollment can also store:

- Enrollment Date
- Attendance
- Fees Paid
- Status

---

## Student → Fees

One Student can have multiple Fee records.

Possible relationship:

- Master-Detail

---

# Important Data Modeling Principles

- Avoid duplicate data
- Use relationships properly
- Choose correct relationship types
- Design scalable systems
- Improve reporting capability

---

# Lookup vs Master-Detail

| Lookup | Master-Detail |
|---|---|
| Loose relationship | Strong relationship |
| Child independent | Child dependent |
| No cascade delete | Cascade delete supported |

---

# Why Data Modeling Matters

Good Data Modeling helps:

- Organize data
- Improve reporting
- Support scalability
- Maintain data quality

---

# Key Takeaways

- Data Modeling designs Salesforce architecture.
- Relationships connect business entities.
- Junction Objects support Many-to-Many relationships.
- Good architecture improves scalability and reporting.
- Salesforce projects start with Data Modeling.

