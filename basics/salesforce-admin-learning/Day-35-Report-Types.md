# Day 39: Custom Report Types in Salesforce

## What is a Report Type?

A Report Type defines which objects, relationships, and fields are available when creating a Salesforce Report.

Simple difference:

- Report Type → Defines the available data structure.
- Report → Uses that structure to analyze actual records.

## Why Report Types are Important

Standard Report Types may not provide the exact object relationships required by a business.

Custom Report Types allow us to create reports such as:

- Patients with Appointments
- Patients with or without Appointments
- Doctors with Appointments

## Custom Report Types Created

### 1. Patients with Appointments

Relationship:

Patients → Appointments

Condition:

`Patients must have at least one related Appointment`

Use case:
Shows only patients who have appointments.

### 2. Patients with or without Appointments

Relationship:

Patients → Appointments

Condition:

`Patients may or may not have related Appointments`

Use case:
Shows all patients, including patients who have no appointments.

### 3. Doctors with Appointments

Relationship:

Doctors → Appointments

Condition:

`Doctors must have at least one related Appointment`

Use case:
Shows doctors who have at least one appointment.

## Important Relationship Concept

When creating a Custom Report Type, Salesforce provides two important relationship options:

`A records must have at least one related B record`

This returns only records where the related record exists.

Example:
Doctors with Appointments

`A records may or may not have related B records`

This can include records where the related record does not exist.

Example:
Patients with or without Appointments

## Hands-On Project

For the Hospital Management System, the following Custom Report Types were created:

1. Patients with Appointments
2. Patients with or without Appointments
3. Doctors with Appointments

These Report Types were deployed and tested by creating reports from them.

## Interview Takeaway

**Q: What is the difference between a Report Type and a Report?**

A: A Report Type defines the objects, relationships, and fields available for reporting, while a Report uses that Report Type to display and analyze actual records.

**Q: Why would you create a Custom Report Type?**

A: When standard Report Types do not provide the required object relationship or fields needed for business reporting.
