# Day 7: Salesforce Security Model – Users, Profiles, Roles & Permission Sets

## Why Security Matters

Organizations store important business information inside Salesforce, including customer details, sales opportunities, and support records.

Not every employee should have access to all data. Salesforce provides a security model that ensures users only receive the access necessary to perform their jobs.

This follows the principle of Least Privilege Access.

---

## User

A User is a person who can log in to Salesforce.

Examples:

- Sales Executive
- Manager
- HR Representative
- Salesforce Administrator

Each User requires:

- Username
- Password
- User License
- Profile

### Important Point

Every Salesforce user must have a valid license.

---

## Profile

A Profile controls what actions a user can perform in Salesforce.

Every user must have exactly one Profile.

Profiles control permissions such as:

- Create
- Read
- Edit
- Delete

These are commonly called CRUD permissions.

### Example

Sales User Profile:

- Create Leads
- View Leads
- Edit Leads
- Cannot Delete Leads

Profiles establish the baseline permissions for users.

---

## CRUD Permissions

### Create

Allows users to create new records.

### Read

Allows users to view records.

### Edit

Allows users to modify records.

### Delete

Allows users to remove records.

---

## Role

A Role controls record visibility within an organization.

While Profiles determine what users can do, Roles determine which records users can see.

### Example

Sales Manager
↓
Sales Executive

The manager can usually view records owned by the sales executive through the role hierarchy.

---

## Role Hierarchy

Organizations often create hierarchical structures such as:

CEO
↓
Sales Director
↓
Sales Manager
↓
Sales Executive

Higher roles generally receive visibility into records owned by lower roles.

This helps managers monitor team performance and activities.

---

## Permission Set

A Permission Set provides additional permissions without modifying a user's Profile.

Permission Sets are commonly used when only a small number of users require extra access.

### Example

A Sales User normally cannot export reports.

If Rahul requires report export access, an Admin can assign a Permission Set instead of creating a new Profile.

---

## Profile vs Permission Set

| Profile | Permission Set |
|----------|---------------|
| Mandatory | Optional |
| One per user | Multiple per user |
| Base permissions | Additional permissions |
| Assigned to all users | Assigned as needed |

---

## Security Layer Summary

### User

Represents the person logging into Salesforce.

### Profile

Controls what actions the user can perform.

### Role

Controls which records the user can access.

### Permission Set

Provides additional permissions beyond the Profile.

---

## Real Business Example

Rahul is a Sales Executive.

Profile:

Sales User

Role:

Sales Executive

Priya is a Sales Manager.

Profile:

Sales Manager

Role:

Sales Manager

Since Priya's role is higher in the hierarchy, she can view records owned by Rahul.

---

## Key Takeaways

- Security is a critical part of Salesforce administration.
- Every User requires a license.
- Every User must have exactly one Profile.
- Profiles control actions and permissions.
- Roles control record visibility.
- Role Hierarchies support management visibility.
- Permission Sets provide additional permissions.
- Users can have multiple Permission Sets.

---

# Interview Questions and Answers

## Q1. What is a User in Salesforce?

**Answer:**

A User is a person who can log in to Salesforce using a valid username, password, license, and profile.

---

## Q2. What is a Profile?

**Answer:**

A Profile controls what actions a user can perform in Salesforce, including permissions such as Create, Read, Edit, and Delete.

---

## Q3. What is the difference between a Profile and a Role?

**Answer:**

A Profile controls what a user can do, while a Role controls which records a user can see.

---

## Q4. Can a User have multiple Profiles?

**Answer:**

No. A Salesforce user can have only one Profile.

---

## Q5. Can a User have multiple Permission Sets?

**Answer:**

Yes. A Salesforce user can have multiple Permission Sets based on business requirements.

---

## Q6. What is a Role Hierarchy?

**Answer:**

A Role Hierarchy is a structure that allows users in higher roles to gain visibility into records owned by users in lower roles.

---

## Q7. Why are Permission Sets preferred over creating many Profiles?

**Answer:**

Permission Sets provide flexibility by granting additional permissions to specific users without creating unnecessary Profile variations.

