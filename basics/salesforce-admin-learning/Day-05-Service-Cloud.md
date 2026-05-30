# Day 5: Service Cloud & Case Management

## What is Service Cloud?

Service Cloud is a Salesforce product designed to help organizations manage customer support, service requests, complaints, and issue resolution.

Its primary goal is to improve customer satisfaction by ensuring that customer issues are tracked and resolved efficiently.

---

## Why Service Cloud is Important

After acquiring customers, organizations must provide effective support to maintain long-term relationships.

Without a proper support system:

- Customer complaints may be lost.
- Support teams may miss deadlines.
- Managers may struggle to track issue resolution.

Service Cloud provides a structured way to manage customer service operations.

---

## What is a Case?

A Case represents a customer issue, complaint, request, or question.

Examples:

- Product defect
- Refund request
- Technical support issue
- Password reset request

Whenever a customer contacts support, a Case is typically created.

### Example

Customer: Rahul Sharma

Issue: Laptop screen not working

Case Number: 1001

Status: New

The issue is now tracked inside Salesforce.

---

## Case Lifecycle

A Case generally moves through multiple stages.

New
↓
Working
↓
Pending Customer
↓
Resolved
↓
Closed

### New

The Case has been created and is awaiting action.

### Working

The support team is actively investigating the issue.

### Pending Customer

Additional information is required from the customer.

### Resolved

The issue has been fixed.

### Closed

The Case is fully completed and no further action is required.

---

## Case Priority

Organizations assign priorities to Cases based on urgency and business impact.

Typical priorities include:

- Low
- Medium
- High
- Critical

### Example

Critical Priority:

A banking application is completely unavailable.

Immediate attention is required.

---

## Case Ownership

Each Case should have an owner responsible for resolving it.

The owner may be:

- Individual support agent
- Support team
- Queue

Proper ownership ensures accountability.

---

## Queues

A Queue is a collection of Cases waiting to be assigned or processed.

Example:

Technical Support Queue

- Case 1
- Case 2
- Case 3

Queues help distribute workload efficiently among support agents.

---

## Service Level Agreement (SLA)

An SLA defines how quickly an organization must respond to and resolve customer issues.

### Example

Critical Issue:

- Response within 1 hour
- Resolution within 4 hours

SLAs help maintain service quality and customer satisfaction.

---

## Escalation

If a Case is not resolved within the expected time, it may be escalated to a higher support level.

Example:

Level 1 Support
↓
Level 2 Support
↓
Manager

Escalation ensures that important issues receive proper attention.

---

## Knowledge Base

A Knowledge Base contains documented solutions to common customer issues.

Examples:

- Password reset instructions
- Installation guides
- Troubleshooting documents

It helps support teams resolve issues faster.

---

## Sales Cloud vs Service Cloud

| Sales Cloud | Service Cloud |
|-------------|---------------|
| Focuses on acquiring customers | Focuses on supporting customers |
| Uses Leads and Opportunities | Uses Cases |
| Revenue-oriented | Service-oriented |
| Used by sales teams | Used by support teams |

---

## Key Takeaways

- Service Cloud manages customer support operations.
- A Case represents a customer issue or request.
- Cases move through multiple statuses.
- Priorities help identify urgent issues.
- Owners are responsible for resolving Cases.
- Queues improve workload distribution.
- SLAs define response and resolution timelines.
- Escalation helps handle unresolved issues.

---

# Interview Questions and Answers

## Q1. What is Service Cloud?

**Answer:**

Service Cloud is a Salesforce product used to manage customer support, complaints, service requests, and issue resolution processes. Its goal is to improve customer satisfaction and service efficiency.

---

## Q2. What is a Case in Salesforce?

**Answer:**

A Case is a record used to track a customer issue, request, complaint, or support inquiry. It helps organizations monitor and resolve customer problems effectively.

---

## Q3. What is Case Ownership?

**Answer:**

Case Ownership refers to assigning responsibility for a Case to a support agent, team, or queue. The owner is accountable for managing and resolving the issue.

---

## Q4. What is a Queue in Salesforce?

**Answer:**

A Queue is a collection of records waiting for assignment or processing. Support agents can access and work on Cases from a queue.

---

## Q5. What is an SLA?

**Answer:**

An SLA (Service Level Agreement) is a commitment that defines expected response and resolution times for customer issues.

---

## Q6. What is Escalation?

**Answer:**

Escalation is the process of transferring unresolved or high-priority Cases to higher support levels or management for faster resolution.

