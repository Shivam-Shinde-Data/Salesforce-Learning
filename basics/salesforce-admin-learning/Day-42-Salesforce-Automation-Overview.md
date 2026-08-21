# Day 42 – Salesforce Automation Overview

## What is Automation?
Salesforce Automation means automatically performing business actions when specific conditions or events occur.

Examples:
- Update records automatically
- Send email notifications
- Create tasks
- Enforce business processes
- Reduce repetitive manual work

## Automation Tools

| Tool | Status | Use |
|---|---|---|
| Workflow Rules | Legacy | Learn for existing/older orgs |
| Process Builder | Legacy | Learn for existing/older orgs |
| Flow Builder | Modern | Primary tool for new automation |
| Approval Processes | Active | Manage approval-based processes |
| Apex | Code-based | Advanced/developer automation |

## Flow Types

### Record-Triggered Flow
Runs automatically when a record is created, updated, or deleted.

Example:
Patient status changes → automatically perform an action.

### Screen Flow
Provides screens for users to enter information.

Example:
Receptionist enters patient details through a guided form.

### Schedule-Triggered Flow
Runs automatically at a scheduled time.

Example:
Daily check for pending appointments.

## Flow Builder Components

### Elements
Building blocks that perform actions or logic.

Examples:
- Get Records
- Create Records
- Update Records
- Delete Records
- Decision
- Screen
- Action

### Connectors
Control the order in which Flow elements execute.

### Resources
Store or calculate values used by the Flow.

Examples:
- Variables
- Formulas
- Choices
- Constants

## Automation Decision Process

Business Requirement
↓
Determine when automation should run
↓
Choose the appropriate automation type
↓
Configure logic and actions
↓
Test and activate

## Important Interview Questions

**What is Salesforce Automation?**  
Automation allows Salesforce to automatically perform business actions based on defined conditions or events.

**What is the modern Salesforce automation tool?**  
Flow Builder.

**What happened to Workflow Rules and Process Builder?**  
They are legacy automation tools. They are mainly relevant when working with existing Salesforce orgs. Flow is recommended for new automation.

**What is a Record-Triggered Flow?**  
A Flow that automatically runs when a record is created, updated, or deleted according to its configuration.

**What is a Screen Flow?**  
A Flow that interacts with users through screens and collects information.

**Screen Flow vs Record-Triggered Flow?**
- Screen Flow → User interaction
- Record-Triggered Flow → Automatic background automation

## Key Takeaway

Modern Salesforce automation is primarily built with **Flow Builder**. Workflow Rules and Process Builder are important mainly for understanding legacy Salesforce implementations, while practical automation development should focus on Flow.
