# Day 8: Record-Level Security – OWD, Sharing Rules & Public Groups

## Introduction

Salesforce security operates at multiple levels:

- Object-Level Security
- Field-Level Security
- Record-Level Security

Record-Level Security determines which specific records a user can access.

This is controlled through OWD, Role Hierarchies, Sharing Rules, Public Groups, and Manual Sharing.

---

## What is OWD?

OWD stands for Organization-Wide Defaults.

OWD defines the default access users have to records they do not own.

It serves as the baseline level of record security in Salesforce.

### Important Principle

Salesforce security is usually designed using the approach:

Most Restrictive Access
↓
Additional Access as Needed

---

## OWD Types

### Private

Users can access only:

- Records they own
- Records shared with them

This is the most restrictive OWD setting.

---

### Public Read Only

Users can:

- View records owned by others

Users cannot:

- Edit records owned by others

---

### Public Read/Write

Users can:

- View records
- Edit records

owned by other users.

---

### Controlled by Parent

Access is inherited from a parent record.

Example:

Contact access may be controlled by the related Account.

---

## Role Hierarchy

Role Hierarchy provides record visibility based on organizational structure.

Example:

Sales Manager
↓
Sales Executive

The manager can typically view records owned by the sales executive.

Role Hierarchy is commonly used to support management reporting and oversight.

---

## Sharing Rules

Sharing Rules automatically grant record access to users or groups beyond the restrictions defined by OWD.

### Types of Sharing Rules

#### Owner-Based Sharing Rule

Shares records based on record ownership.

Example:

Share all records owned by the Sales Team with Managers.

---

#### Criteria-Based Sharing Rule

Shares records based on field values.

Example:

Share Opportunities where Amount > ₹10,00,000 with Senior Management.

---

## Public Groups

A Public Group is a collection of users that can be used when assigning access.

### Example

Sales Team Group:

- Rahul
- Priya
- Amit
- Neha

Instead of assigning permissions individually, administrators can assign access to the entire group.

---

## Manual Sharing

Manual Sharing allows users to share individual records with specific users.

### Example

Rahul owns Opportunity A.

He manually shares it with Amit.

This is useful when only a small number of records require sharing.

---

## Security Access Flow

OWD
↓
Role Hierarchy
↓
Sharing Rules
↓
Manual Sharing

This is the typical order used when designing record-level security.

---

## Real Business Example

OWD:

Private

Users:

- Rahul (Sales Executive)
- Amit (Sales Executive)
- Priya (Sales Manager)

Result:

- Rahul sees only his records.
- Amit sees only his records.
- Priya can see records owned by both Rahul and Amit through the Role Hierarchy.

A Sharing Rule can then be used to provide access to additional teams such as Support.

---

## Key Takeaways

- OWD defines default record access.
- Private is the most restrictive OWD setting.
- Role Hierarchies provide manager visibility.
- Sharing Rules automatically expand access.
- Public Groups simplify access management.
- Manual Sharing is used for specific records.
- Security should be designed from restrictive to open.

---

# Interview Questions and Answers

## Q1. What is OWD in Salesforce?

**Answer:**

OWD (Organization-Wide Defaults) defines the default level of access users have to records they do not own.

---

## Q2. Which OWD setting is the most restrictive?

**Answer:**

Private is the most restrictive OWD setting because users can access only their own records unless additional sharing is provided.

---

## Q3. What is the purpose of Role Hierarchy?

**Answer:**

Role Hierarchy allows users in higher roles to gain visibility into records owned by users in lower roles.

---

## Q4. What is a Sharing Rule?

**Answer:**

A Sharing Rule automatically grants record access to users or groups beyond the access provided by OWD and Role Hierarchy.

---

## Q5. What is the difference between Role Hierarchy and Sharing Rules?

**Answer:**

Role Hierarchy provides access based on organizational structure, while Sharing Rules provide access based on business requirements.

---

## Q6. What is a Public Group?

**Answer:**

A Public Group is a collection of users that simplifies the process of assigning record access and permissions.

---

## Q7. When should Manual Sharing be used?

**Answer:**

Manual Sharing should be used when a small number of individual records need to be shared with specific users.

