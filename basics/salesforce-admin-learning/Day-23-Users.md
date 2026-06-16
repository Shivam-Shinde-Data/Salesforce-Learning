# Day 23: Users in Salesforce

## Introduction

Users are the people who log in and use Salesforce.

Examples:

- Admins
- Employees
- Managers
- Doctors
- Receptionists

Every person using Salesforce requires a User account.

---

# What is a User?

A User is a person who can access Salesforce using:

- Username
- Password

Each user has:

- Profile
- Role
- Permissions
- License

---

# Why Users Are Important

Users help Salesforce:

- Control security
- Manage permissions
- Track activities
- Assign record ownership

---

# Important User Components

| Component | Purpose |
|---|---|
| Username | Login identity |
| Password | Authentication |
| Profile | Controls permissions |
| Role | Controls visibility |
| License | Defines access type |

---

# Username vs Email

| Username | Email |
|---|---|
| Used for login | Used for communication |
| Must be globally unique | Does not need uniqueness |

---

# What is a Profile?

Profile controls:

```text
What a user can do
```

Examples:

- Create records
- Edit records
- Delete records
- Access apps

---

# What is a Role?

Role controls:

```text
What records a user can see
```

Roles create hierarchy inside organization.

Example:

```text
Hospital Director
      ↓
Department Head
      ↓
Doctors
```

---

# Difference Between Profile and Role

| Profile | Role |
|---|---|
| Controls permissions | Controls visibility |
| What user can do | What user can see |

---

# How to View Users

Navigation:

```text
Gear Icon
 ↓
Setup
 ↓
Users
 ↓
Users
```

You will see:

- Username
- Profile
- Active Status
- User Details

---

# Creating a New User

## Steps

```text
Setup
 ↓
Users
 ↓
Users
 ↓
New User
```

Fill:

- Name
- Username
- Email
- Profile

Then Save.

---

# Active vs Inactive User

| Status | Meaning |
|---|---|
| Active | User can login |
| Inactive | User cannot login |

---

# Record Ownership

Every Salesforce record has an Owner.

Example:

| Record | Owner |
|---|---|
| Patient Rahul | Dr. Sharma |

Ownership affects:

- Security
- Visibility
- Reporting

---

# Key Takeaways

- Users are people who access Salesforce.
- Every user has Profile and Role.
- Profile controls permissions.
- Role controls visibility.
- Users improve security and access management.
