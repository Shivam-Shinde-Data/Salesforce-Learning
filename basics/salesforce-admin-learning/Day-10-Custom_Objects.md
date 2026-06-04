# Day 10: Creating Your First Custom Object (`Student__c`)

## Introduction

Salesforce provides Standard Objects such as:

- Account
- Contact
- Lead
- Opportunity

However, organizations often require additional objects based on business needs.

These user-created objects are called Custom Objects.

---

## What is a Custom Object?

A Custom Object is a user-defined database table in Salesforce used to store business-specific information.

Examples:

- Student__c
- Course__c
- Employee__c
- Patient__c

Custom Objects allow Salesforce to support industries beyond CRM.

---

## Standard Object vs Custom Object

| Standard Object | Custom Object |
|----------------|---------------|
| Provided by Salesforce | Created by Administrator |
| CRM-focused | Business-specific |
| Example: Account | Example: Student__c |
| Default in Salesforce | User-created |

---

## Naming Convention

Custom Objects always end with:

__c

Example:

- Student__c
- Course__c
- Faculty__c

This suffix identifies the object as a Custom Object.

---

## Object Components

### Label

The visible name shown to users.

Example:

Student

---

### Plural Label

The plural form of the object name.

Example:

Students

---

### API Name

The internal system name used by Salesforce and developers.

Example:

Student__c

---

## Record Name

Every object requires one primary identifying field called the Record Name.

Example:

Student Name

Salesforce uses this field as the main display value for records.

---

## Record Name Types

### Text

User manually enters values.

Example:

Rahul Sharma

---

### Auto Number

Salesforce automatically generates values.

Example:

STU-0001

---

## Steps to Create Custom Object

1. Open Setup.
2. Open Object Manager.
3. Click Create.
4. Select Custom Object.
5. Enter:
   - Label = Student
   - Plural Label = Students
   - Record Name = Student Name
6. Select Record Name Type = Text.
7. Save the object.

---

## Result

Custom Object Created:

Student__c

This object will be used in the Student Management System project.

---

## Key Takeaways

- Custom Objects are created by administrators.
- Custom Objects store business-specific information.
- Custom Objects end with __c.
- API Names are system/internal names.
- Every object requires a Record Name field.
- Record Name can use Text or Auto Number.
