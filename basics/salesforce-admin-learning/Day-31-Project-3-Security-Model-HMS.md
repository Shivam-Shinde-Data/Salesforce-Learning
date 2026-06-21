# Project 3: Security Model – Hospital Management System

## Project Goal

Design a secure Hospital Management System using Salesforce Security features.

---

# Objects

- Department__c
- Doctor__c
- Patient__c
- Appointment__c
- Billing__c

---

# Profiles

## Hospital Director

- Full Access
- Create, Read, Edit, Delete

---

## Doctor

- Read Patient
- Create Appointment
- Edit Appointment
- Cannot Delete Billing

---

## Receptionist

- Create Patient
- Create Appointment
- Read Billing
- Cannot Delete Records

---

# Role Hierarchy

```text
Hospital Director

↓

Department Head

↓

Doctor

↓

Receptionist
```

Higher roles can access lower role records.

---

# OWD Configuration

| Object | OWD |
|---|---|
| Department | Public Read Only |
| Doctor | Public Read Only |
| Patient | Private |
| Appointment | Private |
| Billing | Private |

---

# Field Level Security

Doctor:

- Name → Visible
- Phone → Visible
- Diagnosis → Visible
- Medical History → Visible

Receptionist:

- Name → Visible
- Phone → Visible
- Diagnosis → Hidden
- Medical History → Hidden

---

# Permission Set

Permission Set:

```text
Senior_Doctor_Access
```

Permissions:

- Export Reports
- Delete Appointment

Assign only to Senior Doctors.

---

# Sharing Rule

Criteria:

```text
Department = Cardiology
```

Share:

```text
Cardiology Patients

↓

Cardiology Doctors
```

Access:

Read Only

---

# Security Architecture

```text
Profiles
   ↓
OWD
   ↓
Role Hierarchy
   ↓
Sharing Rules
   ↓
Field Level Security
   ↓
Permission Sets
```

---

# Key Takeaways

- Profiles control object permissions.
- Roles control record visibility.
- OWD defines default access.
- Sharing Rules expand access.
- FLS secures sensitive fields.
- Permission Sets provide extra permissions.

