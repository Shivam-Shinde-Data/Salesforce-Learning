# Day 11: Creating Custom Fields (`Student__c`)

## Introduction

Fields are used to store information inside Salesforce Objects.

After creating the `Student__c` object, the next step is to add Custom Fields to store student-related data.

Examples:

- Roll Number
- Department
- Email
- Phone
- Admission Date

---

## What is a Field?

A Field is a data element used to store a specific type of information about a record.

Fields are similar to columns in a database table or Excel sheet.

---

## Standard Fields vs Custom Fields

| Standard Fields | Custom Fields |
|---|---|
| Created by Salesforce | Created by Administrator |
| Example: Created Date | Example: Roll Number |
| Available by default | Business-specific |

---

## Important Field Properties

| Property | Meaning |
|---|---|
| Label | Visible name shown to users |
| API Name | Internal system name |
| Data Type | Type of information stored |

---

## Field Types Used

| Field | Type |
|---|---|
| Roll Number | Number |
| Department | Picklist |
| Email | Email |
| Phone | Phone |
| Admission Date | Date |
| Active Student | Checkbox |

---

## Picklist Field

Picklist fields allow users to choose values from predefined options.

Example:

Department:

- Computer Science
- IT
- Mechanical
- Civil

Picklists help maintain consistent data.

---

## Checkbox Field

Checkbox fields store True or False values.

Example:

Active Student = True

---

## Steps to Create Fields

1. Open Setup.
2. Open Object Manager.
3. Select Student Object.
4. Open Fields & Relationships.
5. Click New.
6. Select Field Type.
7. Enter Label and other details.
8. Save the field.

---

## Fields Created

Inside `Student__c`:

- Student Name
- Roll Number
- Department
- Email
- Phone
- Admission Date
- Active Student

---

## Key Takeaways

- Fields store information inside objects.
- Different field types exist for different data.
- Picklists standardize user input.
- Checkbox fields store Yes/No values.
- API Names are internal field names used by Salesforce.

---
