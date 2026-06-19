# Day 28: Sharing Rules in Salesforce

## What are Sharing Rules?

Sharing Rules automatically share records with specific:

- Users
- Roles
- Public Groups

They provide additional access beyond OWD.

---

# Why Sharing Rules?

Suppose:

OWD:

```text
Patient = Private
```

Doctors can only see their own patients.

If Hospital wants Cardiology doctors to share records,

we create:

**Sharing Rules**

---

# OWD vs Sharing Rules

| OWD | Sharing Rules |
|---|---|
| Restricts access | Expands access |
| Default security | Additional sharing |
| Starting point | Extra visibility |

---

# Types of Sharing Rules

## 1. Owner Based Sharing Rule

Shares records based on:

```text
Record Owner
```

Example:

Share Doctor owned Patients

with

Department Head.

---

## 2. Criteria Based Sharing Rule

Shares records based on:

```text
Field Values
```

Example:

```text
Department = Cardiology
```

Share with:

```text
Cardiology Doctors
```

---

# Security Model

```text
Profile
 ↓
OWD
 ↓
Role Hierarchy
 ↓
Sharing Rules
 ↓
Manual Sharing
```

---

# Important Rule

Sharing Rules:

✅ Expand Access

❌ Cannot Restrict Access

---

# Hands-On

Navigation:

```text
Gear Icon
 ↓
Setup
 ↓
Sharing Settings
 ↓
Sharing Rules
```

Try:

- Owner Based Rule
- Criteria Based Rule

---

# Key Takeaways

- Sharing Rules provide additional record access.
- OWD restricts access.
- Sharing Rules expand access.
- Two types: Owner Based and Criteria Based.
- Sharing Rules are part of Record Level Security.

