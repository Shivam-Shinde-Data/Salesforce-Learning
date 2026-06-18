# Day 27: OWD (Organization-Wide Defaults)

## What is OWD?

OWD stands for:

**Organization-Wide Defaults**

It defines:

```text
Default record access in Salesforce.
```

OWD controls:

- Record Visibility
- Record Level Security

---

# OWD Types

| OWD Type | Meaning |
|---|---|
| Private | Only Owner can access |
| Public Read Only | Everyone can read |
| Public Read/Write | Everyone can read and edit |
| Controlled by Parent | Parent controls access |

---

# Example

Patient Object:

OWD:

```text
Private
```

Doctor Rahul:

Can see:

- His own Patients

Cannot see:

- Other Doctor's Patients

---

# Controlled By Parent

Example:

```text
Patient
   ↓
Billing
```

If Billing OWD:

```text
Controlled By Parent
```

Then Billing access depends on Patient access.

---

# Security Hierarchy

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

# Difference

| Feature | Purpose |
|---|---|
| Profile | What user can do |
| Permission Set | Extra permissions |
| Role | Record visibility hierarchy |
| OWD | Default record access |

---

# Hands-On

Navigation:

```text
Gear Icon
 ↓
Setup
 ↓
Sharing Settings
```

Observe:

- Student OWD
- Course OWD
- Standard Object OWD

---

# Key Takeaways

- OWD controls default record access.
- OWD is part of Record Level Security.
- Private is the most secure option.
- Controlled By Parent is commonly used with Master-Detail.
- OWD works together with Roles and Sharing Rules.
