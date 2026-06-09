# Day 15: Creating Course Object (`Course__c`)

## Introduction

After creating the Student Object, the next step is to create a Course Object for storing course-related information.

Salesforce applications usually contain multiple objects representing different business entities.

---

## What is a Course Object?

The Course Object stores information related to courses offered by a college or institution.

Examples:

- Java Full Stack
- Python Programming
- Cloud Computing

---

## Why Separate Objects Are Important

Different business entities should be stored in separate objects.

Examples:

| Entity | Object |
|---|---|
| Student | Student__c |
| Course | Course__c |

This improves:

- Data organization
- Scalability
- Data management
- Application structure

---

## Course Object Fields

| Field | Type |
|---|---|
| Course Name | Record Name |
| Course Code | Text |
| Duration | Number |
| Fees | Currency |
| Department | Picklist |
| Active Course | Checkbox |

---

## Steps to Create Course Object

1. Open Setup.
2. Open Object Manager.
3. Click Create → Custom Object.
4. Enter:
   - Label = Course
   - Plural Label = Courses
   - Record Name = Course Name
5. Save the object.

---

## Steps to Create Fields

Inside Course Object:

1. Open Fields & Relationships.
2. Click New.
3. Create fields:
   - Course Code
   - Duration
   - Fees
   - Department
   - Active Course

---

## Creating Course Tab

1. Open Setup.
2. Search Tabs.
3. Under Custom Object Tabs click New.
4. Select Course Object.
5. Choose tab style.
6. Save.

---

## Sample Course Records

| Course Name | Course Code | Fees |
|---|---|---|
| Java Full Stack | JAVA101 | 45000 |
| Python Programming | PY201 | 30000 |
| Cloud Computing | CLD301 | 50000 |

---

## Key Takeaways

- Salesforce applications contain multiple objects.
- Each object represents a business entity.
- Custom Objects end with `__c`.
- Objects help organize business data properly.
- Multi-object architecture is common in Salesforce.
