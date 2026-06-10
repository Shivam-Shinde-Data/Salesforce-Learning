# Project 1: Student Management System v1

## Project Overview

The Student Management System is a Salesforce-based application used to manage students and courses.

The system stores student information, course information, and relationships between students and courses.

---

# Objects Used

| Object | Purpose |
|---|---|
| Student__c | Stores student data |
| Course__c | Stores course data |

---

# Student Object Fields

| Field | Type |
|---|---|
| Student Name | Text |
| Roll Number | Number |
| Department | Picklist |
| Email | Email |
| Phone | Phone |
| Admission Date | Date |
| Active Student | Checkbox |
| Course | Lookup(Course) |

---

# Course Object Fields

| Field | Type |
|---|---|
| Course Name | Text |
| Course Code | Text |
| Duration | Number |
| Fees | Currency |
| Department | Picklist |
| Active Course | Checkbox |

---

# Relationship Used

## Lookup Relationship

```text
Student__c
   ↓
Course__c
```

Students are connected to Courses using a Lookup Relationship.

---

# Features Implemented

- Custom Objects
- Custom Fields
- Custom Tabs
- Page Layouts
- Record Creation
- Lookup Relationships
- CRUD Operations
- List Views

---

# CRUD Operations

| Operation | Meaning |
|---|---|
| Create | Add records |
| Read | View records |
| Update | Modify records |
| Delete | Remove records |

---

# Project Workflow

```text
Course Created
      ↓
Student Created
      ↓
Student Assigned To Course
```

---

# Sample Data

| Student | Course |
|---|---|
| Rahul Sharma | Java Full Stack |
| Priya Patil | Python Programming |
| Shivam Shinde | Cloud Computing |

---

# Key Learnings

- Salesforce application structure
- Multi-object architecture
- Relationships between objects
- Record management
- UI customization
- Business data organization
