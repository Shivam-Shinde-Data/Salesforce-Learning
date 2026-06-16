# Day 24: Profiles in Salesforce

## What is a Profile?

A Profile controls:

```text
What a user CAN do inside Salesforce.
```

Profiles define:

- Object Permissions
- Field Permissions
- App Access
- Tab Visibility
- Administrative Permissions

---

# Profile vs Role

| Profile | Role |
|---|---|
| Controls permissions | Controls visibility |
| What user can do | What user can see |
| Create/Edit/Delete | Record Hierarchy |

---

# CRUD Permissions

Profiles control:

| Permission | Meaning |
|---|---|
| Create | Create records |
| Read | View records |
| Update | Edit records |
| Delete | Delete records |

This is called:

**CRUD**

---

# Field Level Security

Profiles can:

- Show fields
- Hide fields
- Make fields Read Only

Example:

Doctor can view Diagnosis.

Receptionist cannot view Diagnosis.

---

# App Permissions

Profiles decide:

Which apps users can access.

Example:

- Hospital App ✅
- HR App ❌

---

# System Administrator Profile

The System Administrator profile has:

- Full Object Access
- Full Setup Access
- User Management
- Security Settings
- App Creation

---

# Hands-On

Navigate:

```text
Gear Icon
 ↓
Setup
 ↓
Profiles
```

Open:

- System Administrator
- Standard User

Compare:

- Object Permissions
- Field Permissions
- App Access

---

# Key Takeaways

- Profiles control what users can do.
- CRUD permissions are controlled by Profiles.
- Profiles manage field security.
- Profiles control app and tab access.
- Profiles are a major part of Salesforce Security.

