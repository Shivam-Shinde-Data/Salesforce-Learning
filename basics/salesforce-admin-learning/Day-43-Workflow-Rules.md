# Day 43 – Workflow Rules

## Overview

Workflow Rules are a legacy Salesforce automation tool used to automatically perform actions when a record meets defined criteria.

Workflow Rules are important for understanding older Salesforce implementations, while Flow Builder is the recommended tool for new automation.

## Workflow Rule Structure

Record Created / Updated
        ↓
Workflow Rule
        ↓
Check Criteria
        ↓
Criteria Met?
        ↓
Workflow Action

## Evaluation Criteria

A Workflow Rule can evaluate records when:

1. A record is created.
2. A record is created and every time it is edited.
3. A record is created and whenever it is edited to subsequently meet the criteria.

The third option is useful when an existing record changes from not meeting the condition to meeting it.

## Rule Criteria

Criteria determine when the Workflow Rule should execute.

Examples:

Age > 60

Status = "Emergency"

Criteria can be configured using fields, operators, values, and formula expressions.

## Workflow Actions

Workflow Rules can perform actions such as:

- Field Update
- Email Alert
- Task
- Outbound Message

### Field Update

Automatically changes a field value.

Example:

Patient Status → Follow-up Required

### Email Alert

Automatically sends an email notification when the rule criteria are met.

### Task

Automatically creates a task for a user.

Example:

Patient Age > 60
        ↓
Create Follow-Up Task

### Outbound Message

Sends information from Salesforce to an external system using Salesforce's legacy outbound messaging mechanism.

## Hands-On Example – Hospital Management System

### Business Requirement

Create a Workflow Rule for the Patient object that identifies senior patients.

### Rule

Object: Patient
Rule Name: Senior_Patient_Follow_Up
Criteria: Age__c > 60

### Evaluation

Record is created

OR

Existing record is edited and subsequently meets the criteria

### Intended Workflow Action

Age > 60
   ↓
Create Task
   ↓
Senior Patient Follow-Up

The task can be configured with:

- Status: Not Started
- Priority: Normal
- Subject: Senior Patient Follow-Up
- Due Date: 0 days

## Important Salesforce Concept

Workflow Rules are legacy automation.

For new Salesforce automation:

Workflow Rules
      ↓
Process Builder
      ↓
Flow Builder

Flow Builder is the primary modern automation tool and provides significantly more flexibility.

## Workflow Rules vs Flow

| Workflow Rules | Flow |
|---|---|
| Legacy automation | Modern automation |
| Simple automation | Simple to complex automation |
| Limited actions | Many elements and actions |
| Mainly existing implementations | Recommended for new automation |
| Less flexible | Highly flexible |

## Interview Questions

### What is a Workflow Rule?

A Workflow Rule automatically performs an action when a record meets specified criteria.

### What are the main workflow actions?

- Field Update
- Email Alert
- Task
- Outbound Message

### What is the difference between Workflow Rule and Flow?

Workflow Rules provide limited, legacy automation capabilities, while Flow provides modern and much more powerful automation capabilities.

### Should you create a new Workflow Rule today?

Normally no. For new automation, Flow Builder should be preferred. Workflow Rules are mainly relevant when maintaining or understanding existing Salesforce implementations.

### What is the purpose of evaluation criteria?

Evaluation criteria determine when Salesforce evaluates a record against the Workflow Rule.

## Key Takeaways

- Workflow Rules are a legacy automation tool.
- They execute when defined criteria are met.
- They can perform field updates, email alerts, tasks, and outbound messages.
- Evaluation criteria control when Salesforce checks the rule.
- Workflow Rules are still important for interviews and legacy orgs.
- Flow Builder is the main automation skill to focus on going forward.
