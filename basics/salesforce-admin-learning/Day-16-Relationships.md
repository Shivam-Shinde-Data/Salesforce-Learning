# Day 16: Relationships in Salesforce

## Introduction

Relationships are used to connect objects in Salesforce.

Real business applications require connected data.

Example:

A Student studies a Course.

This connection is created using Relationships.

---

## What is a Relationship?

A Relationship is a connection between two Salesforce objects.

Relationships help organize and connect business data.

---

## Types of Relationships

| Relationship Type | Purpose |
|---|---|
| Lookup Relationship | Loose connection between objects |
| Master-Detail Relationship | Strong parent-child relationship |

---

## Lookup Relationship

A Lookup Relationship creates a connection between two objects while keeping both objects independent.

Example:

Student → Course

A Student record can reference a Course record.

---

## Master-Detail Relationship

Master-Detail creates a strong parent-child relationship.

Features:

- Child depends on Parent
- Parent controls security
- Deleting parent deletes child

---

## Lookup vs Master-Detail

| Feature | Lookup | Master-Detail |
|---|---|---|
| Relationship Strength | Loose | Strong |
| Child Independent | Yes | No |
| Parent Controls Security | No | Yes |
| Parent Deletion Deletes Child | No | Yes |

---

## Steps to Create Lookup Relationship

1. Open Setup.
2. Open Object Manager.
3. Open Student Object.
4. Open Fields & Relationships.
5. Click New.
6. Select Lookup Relationship.
7. Related Object = Course.
8. Field Label = Course.
9. Save.

---

## Relationship Structure

```text
Course (Parent)
   ↓
Student (Child)
```

Students can now reference Courses.

---

## Key Takeaways

- Relationships connect objects.
- Lookup Relationships create loose connections.
- Master-Detail creates strong parent-child structures.
- Relationships reduce duplicate data.
- Salesforce applications rely heavily on relationships.
