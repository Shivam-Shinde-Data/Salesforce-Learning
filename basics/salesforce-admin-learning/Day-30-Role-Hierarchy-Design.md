# Day 30: Role Hierarchy Design

## What is Role Hierarchy?

Role Hierarchy is a tree structure that allows:

```text
Higher Roles

↓

Access Records Owned By

↓

Lower Roles
```

It controls record visibility in Salesforce.

---

# Hospital Hierarchy Example

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

Lower roles cannot access higher role records.

---

# Role vs Profile

| Profile | Role |
|---|---|
| Controls permissions | Controls record visibility |
| Create, Edit, Delete | Record access hierarchy |
| Object level | Record level |

---

# Example

Receptionist creates:

```text
Patient Registration
```

Access:

| User | Can See |
|---|---|
| Receptionist | Yes |
| Doctor | Yes |
| Department Head | Yes |
| Hospital Director | Yes |

---

# Important Rule

```text
Higher Role

Can See

Lower Role Records
```

```text
Lower Role

Cannot See

Higher Role Records
```

---

# How to Create Roles

Navigation:

```text
Gear Icon
 ↓
Setup
 ↓
Roles
 ↓
Add Role
```

Create:

- Hospital Director
- Department Head
- Doctor
- Receptionist

---

# Key Takeaways

- Role Hierarchy controls record visibility.
- Higher roles can access lower role records.
- Roles do not give object permissions.
- Profiles control permissions.
- Role design is important for Salesforce security.
