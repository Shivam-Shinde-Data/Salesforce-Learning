# Day 3: Salesforce Architecture

## What is Salesforce Architecture?

Salesforce Architecture refers to the underlying design and structure that allows Salesforce to provide CRM services to thousands of organizations through a single cloud platform.

Unlike traditional software, companies do not need to manage servers, databases, or infrastructure. Salesforce handles these responsibilities while organizations focus on using the platform.

---

## Multi-Tenant Architecture

One of the most important concepts in Salesforce is Multi-Tenant Architecture.

A tenant represents a customer using Salesforce.

In a multi-tenant model, multiple organizations share the same Salesforce infrastructure while keeping their data, users, and configurations separate and secure.

### Example

Think of an apartment building:

- Many families live in the same building.
- Infrastructure is shared.
- Each family has its own private apartment.

Similarly:

- Multiple companies use Salesforce.
- Infrastructure is shared.
- Data remains isolated.

### Benefits

- Lower infrastructure costs
- Automatic platform updates
- Better scalability
- Improved maintenance
- High security

---

## Metadata-Driven Architecture

Salesforce is built on a Metadata-Driven Architecture.

Metadata means "data about data."

Instead of manually changing database structures and application code, Salesforce stores configurations as metadata.

Examples of metadata include:

- Objects
- Fields
- Page Layouts
- Reports
- Dashboards
- Flows
- Security Settings

### Why Metadata is Important

Because of metadata, Salesforce Administrators can:

- Create applications quickly
- Add new fields
- Modify layouts
- Build automations

without writing code.

---

## Objects, Records, and Fields

These are the building blocks of Salesforce.

### Object

An Object is used to store a specific type of information.

Examples:

- Student
- Employee
- Account
- Contact

### Database Comparison

Table = Object

---

### Record

A Record is a single entry stored inside an Object.

Example:

Student Name: Rahul Sharma

This student entry represents one record.

### Database Comparison

Row = Record

---

### Field

A Field stores a specific piece of information.

Examples:

- Name
- Email
- Phone Number
- Admission Date

### Database Comparison

Column = Field

---

## Salesforce vs Database Terminology

| Database | Salesforce |
|-----------|------------|
| Table | Object |
| Row | Record |
| Column | Field |

This comparison is important for candidates who already know SQL and database concepts.

---

## Standard Objects

Standard Objects are provided by Salesforce and support common business processes.

Examples:

- Lead
- Account
- Contact
- Opportunity
- Case

These objects are available immediately after setting up Salesforce.

---

## Custom Objects

Custom Objects are created by users to support specific business requirements.

Examples:

- Student
- Course
- Faculty
- Library Book
- Patient

Organizations create Custom Objects when Standard Objects do not meet their needs.

---

## Real-World Example

Suppose a college wants to manage student information using Salesforce.

The Admin can create:

### Student Object

Fields:

- Student Name
- Roll Number
- Email
- Mobile Number
- Admission Date

Each student entered into Salesforce becomes a record inside the Student Object.

This allows the college to manage student information efficiently.

---

## Key Takeaways

- Salesforce uses Multi-Tenant Architecture.
- Multiple organizations share the same infrastructure.
- Salesforce uses Metadata-Driven Architecture.
- Objects store data.
- Records represent individual entries.
- Fields store specific information.
- Standard Objects are provided by Salesforce.
- Custom Objects are created based on business requirements.

---

# Interview Questions and Answers

## Q1. What is Salesforce Architecture?

**Answer:**

Salesforce Architecture is the design and structure that enables Salesforce to provide cloud-based CRM services using shared infrastructure, metadata-driven customization, and scalable technologies.

---

## Q2. What is Multi-Tenant Architecture?

**Answer:**

Multi-Tenant Architecture is a model in which multiple organizations share the same Salesforce infrastructure while keeping their data, configurations, and users isolated and secure.

---

## Q3. What is Metadata in Salesforce?

**Answer:**

Metadata is data that describes the structure and configuration of Salesforce components such as objects, fields, reports, page layouts, and security settings.

---

## Q4. What is an Object in Salesforce?

**Answer:**

An Object is a database-like structure used to store a particular type of information. Examples include Account, Contact, and custom objects such as Student.

---

## Q5. What is the difference between a Standard Object and a Custom Object?

**Answer:**

Standard Objects are provided by Salesforce by default, such as Account and Contact. Custom Objects are created by organizations to meet specific business requirements, such as Student or Patient objects.

---

## Q6. How do Objects, Records, and Fields relate to database concepts?

**Answer:**

Objects are similar to database tables, Records are similar to rows, and Fields are similar to columns.

---
