# Day 12: Creating Custom Tabs & Navigating Your Student App

## Introduction

After creating Custom Objects and Fields, users still need a way to access the application easily.

Salesforce uses Tabs for navigation.

Tabs allow users to open objects, records, reports, dashboards, and applications directly from the user interface.

---

## What is a Tab?

A Tab is a navigation component in Salesforce used to access objects and related records.

Tabs improve application usability and navigation.

Examples:

- Accounts
- Contacts
- Leads
- Students

---

## Standard Tabs vs Custom Tabs

| Standard Tabs | Custom Tabs |
|---|---|
| Provided by Salesforce | Created by Administrator |
| Linked to Standard Objects | Linked to Custom Objects |
| Example: Accounts | Example: Students |

---

## Types of Tabs

### Custom Object Tab

Used for accessing Custom Objects.

Example:

Student__c

---

### Web Tab

Used to open external websites.

---

### Visualforce Tab

Used for Visualforce pages created by developers.

---

## Why Tabs Are Important

Tabs help users:

- Navigate easily
- Access records quickly
- Use applications efficiently

Without tabs, users cannot easily access custom objects.

---

## Steps to Create Custom Tab

1. Open Setup.
2. Search Tabs in Quick Find.
3. Open Tabs.
4. Under Custom Object Tabs click New.
5. Select Object = Student.
6. Choose Tab Style.
7. Save the tab.

---

## Creating First Student Record

Inside Student Tab:

1. Click New.
2. Enter student details.
3. Save the record.

Example:

| Field | Value |
|---|---|
| Student Name | Rahul Sharma |
| Roll Number | 101 |
| Department | Computer Science |
| Email | rahul@gmail.com |

---

## Application Flow

```text
Object
   ↓
Fields
   ↓
Tab
   ↓
Records
```

This represents the basic Salesforce application structure.

---

## Key Takeaways

- Tabs improve navigation.
- Custom Tabs are created for Custom Objects.
- Tabs help users access records easily.
- Salesforce applications become usable after adding tabs.
- Records are created through object tabs.
