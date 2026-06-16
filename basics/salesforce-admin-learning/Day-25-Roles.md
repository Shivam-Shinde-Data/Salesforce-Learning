# Day 29: Roles in Salesforce

## What is a Role?

A Role controls:

```text
What records a user CAN SEE.
```

Roles create a hierarchy for record visibility inside Salesforce.

---

# Role Hierarchy Example

```text
Hospital Director
      ↓
Department Head
      ↓
Doctor
      ↓
Receptionist
```

Higher roles can usually see records owned by lower roles.

---

# Real Example

Doctor Rahul creates:

```text
Patient: Amit Sharma
```

Department Head can see:

- Amit Sharma

Doctor Rahul can see:

- His own records

---

# Role Does NOT Control

Roles do NOT control:

- Create
- Edit
- Delete
- Object Permissions

These are controlled by:

**Profiles**

---

# How to View Roles

Navigation:

```text
Gear Icon
 ↓
Setup
 ↓
Roles
```

You can:

- View hierarchy
- Create new roles
- Manage record visibility

---

# Hospital Role Hierarchy

```text
Hospital Director
      ↓
Department Head
      ↓
Doctor
      ↓
Receptionist
```

---

# Key Takeaways

- Roles control record visibility.
- Profiles control permissions.
- Higher roles can access lower role records.
- Roles create hierarchy inside Salesforce.
- Roles are an important part of Salesforce Security.

