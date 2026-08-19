# Day 48 – Process Builder

## Overview

Process Builder was a declarative Salesforce automation tool used to create more advanced automation than Workflow Rules.

It is now a **legacy automation tool**. Salesforce recommends **Flow Builder** for new automation.

## Process Builder Structure

Record Created / Updated
        ↓
Process Builder
        ↓
Check Criteria
        ↓
Criteria Met?
        ↓
Automation Action

## Main Concepts

### Object
The object whose record starts the process.

Example:
Appointment

### Start Criteria
Determines when the process starts.

Examples:
- Record is created
- Record is created or edited

### Criteria
Defines when an action should execute.

Example:

Status = Completed

### Actions

Process Builder could perform actions such as:

- Create Records
- Update Records
- Send Email Alerts
- Create Tasks
- Invoke Flows
- Invoke other Processes
- Post to Chatter

## Practical HMS Example

### Requirement

When an Appointment becomes Completed, automatically update the related Patient record.

### Legacy Process Builder Logic

Appointment Updated
        ↓
Status = Completed?
        ↓
YES
        ↓
Update Patient

## Process Builder vs Workflow Rules

| Workflow Rules | Process Builder |
|---|---|
| Legacy | Legacy |
| Simpler automation | More advanced automation |
| Limited actions | More action types |
| Field updates, emails, tasks | Create/update records, emails, tasks, Flow invocation |
| Less flexible | More flexible |

## Process Builder vs Flow

| Process Builder | Flow |
|---|---|
| Legacy | Modern |
| Limited logic | Powerful logic and branching |
| No user interaction | Supports Screen Flows |
| Limited data operations | Extensive data operations |
| Not recommended for new automation | Recommended for new automation |

## Why Process Builder Was Replaced

As Salesforce automation became more complex, maintaining multiple automation tools became difficult. Salesforce consolidated automation capabilities into Flow Builder.

Therefore:

**Workflow Rules → Process Builder → Flow**

Today:

**Flow Builder is the preferred tool for new automation.**

## Interview Questions

### What is Process Builder?

Process Builder was a declarative Salesforce automation tool used to perform actions when records met specified criteria.

### Is Process Builder recommended for new automation?

No. It is a legacy tool. Flow Builder should be used for new automation.

### What could Process Builder do?

- Create records
- Update records
- Send email alerts
- Create tasks
- Invoke Flows
- Invoke other Processes
- Post to Chatter

### Process Builder vs Workflow Rule?

Process Builder provided more advanced automation capabilities than Workflow Rules, including creating and updating records and invoking other automation.

### Process Builder vs Flow?

Flow is the modern replacement and provides more powerful logic, branching, data operations, user interaction, debugging, and automation capabilities.

## Key Takeaways

- Process Builder is a legacy automation tool.
- It provided more capabilities than Workflow Rules.
- It could create/update records and invoke other automation.
- It is important for understanding existing Salesforce orgs and interviews.
- Flow Builder is the modern replacement and should be used for new automation.
