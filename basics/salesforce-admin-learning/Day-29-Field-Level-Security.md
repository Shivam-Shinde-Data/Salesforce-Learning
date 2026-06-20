# Day 33: Field Level Security (FLS)

## What is Field Level Security?

Field Level Security (FLS) controls:

```text
Can a user see a field?

Can a user edit a field?
```

It provides security at the field level.

---

# Field Access Types

| Access Type | Meaning |
|---|---|
| Visible + Editable | User can see and edit |
| Visible + Read Only | User can see but cannot edit |
| Hidden | User cannot see the field |

---

# Example

Patient Object:

| Field | Doctor | Receptionist |
|---|---|---|
| Name | Visible | Visible |
| Phone | Visible | Visible |
| Diagnosis | Visible | Hidden |
| Medical History | Visible | Hidden |

---

# Profile vs FLS

| Profile | Field Level Security |
|---|---|
| Object permissions | Field permissions |
| Controls Create/Edit/Delete | Controls View/Edit field |
| Object level | Field level |

---

# Important Rule

Even if:

```text
Profile = Edit Patient
```

If:

```text
Diagnosis = Read Only
```

Then:

User cannot edit Diagnosis.

---

# How to Configure FLS

Navigation:

```text
Object Manager
 ↓
Student
 ↓
Fields & Relationships
 ↓
Select Field
 ↓
Set Field-Level Security
```

---

# Key Takeaways

- FLS controls field visibility and edit access.
- Fields can be Hidden, Read Only, or Editable.
- FLS provides security at field level.
- FLS overrides object-level edit permissions.
- FLS is an important part of Salesforce Security.

