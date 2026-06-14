# Project 2: Hospital Management System

## Introduction

This project demonstrates Salesforce Data Modeling using a Hospital Management System.

The system manages:

* Patients
* Doctors
* Departments
* Appointments
* Billing

This project helps understand:

* Objects
* Relationships
* Junction Objects
* Data Modeling
* Business Architecture

---

# Business Requirements

The hospital wants a system to manage:

* Patient records
* Doctor records
* Department management
* Appointment tracking
* Billing information

---

# Objects

| Business Entity | Salesforce Object |
| --------------- | ----------------- |
| Patient         | Patient__c        |
| Doctor          | Doctor__c         |
| Department      | Department__c     |
| Appointment     | Appointment__c    |
| Billing         | Billing__c        |

---

# Department Object

| Field              | Type           |
| ------------------ | -------------- |
| Department Name    | Text           |
| Department Code    | Text           |
| Floor Number       | Number         |
| Head of Department | Text           |
| Description        | Long Text Area |

---

# Department Role in System

Department object is used to organize doctors into different hospital departments.

Examples:

* Cardiology
* Neurology
* Orthopedics
* Pediatrics

---


# Example

| Department | Doctor     |
| ---------- | ---------- |
| Cardiology | Dr. Sharma |
| Cardiology | Dr. Mehta  |
| Neurology  | Dr. Verma  |

---

# Patient Object

| Field        | Type           |
| ------------ | -------------- |
| Patient Name | Text           |
| Age          | Number         |
| Phone        | Phone          |
| Blood Group  | Picklist       |
| Address      | Long Text Area |

---

# Doctor Object

| Field          | Type     |
| -------------- | -------- |
| Doctor Name    | Text     |
| Specialization | Picklist |
| Experience     | Number   |
| Phone          | Phone    |

---

# Appointment Object

| Field            | Type           |
| ---------------- | -------------- |
| Appointment Date | Date           |
| Status           | Picklist       |
| Diagnosis        | Long Text Area |
| Notes            | Long Text Area |

---

# Billing Object

| Field          | Type     |
| -------------- | -------- |
| Bill Amount    | Currency |
| Payment Status | Picklist |
| Payment Date   | Date     |

---

# Relationships

## Department → Doctor

One Department can contain many Doctors.

Relationship Type:

* Lookup Relationship

---

## Patient ↔ Doctor

One Patient can visit many Doctors.

One Doctor can treat many Patients.

This becomes:

* Many-to-Many Relationship

Solution:

* Junction Object

---

# Appointment Object as Junction Object

Appointment__c acts as Junction Object.

Structure:

```text
Patient
   ↓
Appointment
   ↑
Doctor
```

Appointment stores:

* Appointment Date
* Diagnosis
* Notes
* Status

---

## Patient → Billing

One Patient can have multiple Bills.

Relationship Type:

* Master-Detail Relationship

---

# Complete Architecture

```text
Department
   ↓
Doctor
   ↑
Appointment
   ↓
Patient
   ↓
Billing
```

---

# Why Appointment Object Is Important

Appointment object is very important because it stores hospital visit information.

Without Appointment object:

* No appointment tracking
* No diagnosis history
* No patient visit records
* No doctor visit management

Appointment acts as bridge object between Patient and Doctor.

---

# Relationship Types

| Relationship        | Type            |
| ------------------- | --------------- |
| Department → Doctor | Lookup          |
| Patient ↔ Doctor    | Many-to-Many    |
| Appointment         | Junction Object |
| Patient → Billing   | Master-Detail   |

---

# Key Learnings

* Salesforce projects are built using Data Modeling.
* Objects represent business entities.
* Relationships connect business data.
* Junction Objects solve Many-to-Many relationships.
* Good architecture improves scalability and reporting.

---

# Real-World Understanding

This project simulates how hospitals manage:

* Patients
* Doctors
* Appointments
* Departments
* Billing systems

inside Salesforce.

