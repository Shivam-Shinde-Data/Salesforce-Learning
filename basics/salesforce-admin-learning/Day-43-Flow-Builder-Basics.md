# Day 43 – Flow Builder Basics

## Overview

Flow Builder is Salesforce's modern declarative automation tool. It allows Admins to automate business processes without writing Apex code.

Flow can be used to:

- Get records
- Create records
- Update records
- Delete records
- Make decisions
- Collect user input
- Send emails
- Perform actions
- Automate business processes

## Flow Builder Structure

Trigger / Start
      ↓
Logic
      ↓
Data / Actions
      ↓
Result

## Current Flow Builder UI

Salesforce's current Flow Builder uses **Auto-Layout by default**. In Auto-Layout, elements are added using the **+ Add Element** button between elements instead of dragging them manually.

Important UI areas:

- Start – beginning of the Flow
- + Add Element – add Flow elements
- End – end of the Flow
- Auto-Layout – automatically organizes the Flow
- Toggle Toolbox – opens the Toolbox/Manager
- Show Errors/Warnings – displays Flow issues
- Debug – tests the Flow
- Save – saves the Flow version
- Activate – makes the Flow available for use

## Important Flow Elements

### Get Records
Retrieves Salesforce records.

Example:
Find a Patient record using its Name or ID.

### Create Records
Creates a new Salesforce record.

### Update Records
Updates an existing Salesforce record.

### Delete Records
Deletes Salesforce records.

### Decision
Creates different paths based on conditions.

Example:

Age > 60?
→ Yes: Create Follow-Up Task
→ No: Continue

### Assignment
Changes or stores values in Flow variables.

### Loop
Processes multiple records one by one.

### Screen
Creates a user interface for collecting information.

### Action
Performs an action such as sending an email or invoking another Salesforce capability.

## Flow Resources

Resources store or calculate information used by a Flow.

Examples:

- Variables
- Formulas
- Constants
- Choices

## Hands-On – Get Records

Created an **Autolaunched Flow (No Trigger)** to understand the basic Flow Builder interface and data retrieval.

### Flow Structure

Start
  ↓
Get Patient
  ↓
End

### Get Records Configuration

Object:
Patient

Filter:
Name → Equals → Existing Patient Name

Record Storage:
- Store only the first record
- Automatically store the record's fields

The Get Records element retrieves the matching Patient record for use by later Flow elements.

## Auto-Layout

Auto-Layout automatically arranges Flow elements in a structured path.

Adding an element:

+ Add Element
→ Select Element
→ Configure Element
→ Done

The element is automatically connected to the Flow path.

## Debugging

Before activating a Flow, use **Debug** to test its behavior and identify errors.

Debugging helps verify:

- Whether the Flow runs correctly
- Whether records are retrieved
- Whether conditions work correctly
- Whether data is processed as expected

## Autolaunched Flow

An Autolaunched Flow runs without directly displaying screens to a user.

It can be called by other automation, actions, Apex, or other supported mechanisms.

We used **Autolaunched Flow (No Trigger)** today only to learn Flow Builder and the Get Records element.

## Important Flow Concepts

Remember:

Get → Create → Update → Delete → Decision → Assignment → Loop → Screen → Action

## Flow vs Legacy Automation

| Workflow Rules | Process Builder | Flow |
|---|---|---|
| Legacy | Legacy | Modern |
| Limited automation | More advanced legacy automation | Highly flexible |
| Simple actions | More action types | Complex logic and data operations |
| Existing orgs | Existing orgs | Recommended for new automation |

## Interview Questions

### What is Flow Builder?

Flow Builder is Salesforce's declarative automation tool used to automate business processes without writing code.

### What is Get Records?

Get Records retrieves Salesforce records that match specified conditions.

### What is Auto-Layout?

Auto-Layout automatically organizes Flow elements into a structured path, making the Flow easier to build and maintain.

### What is an Autolaunched Flow?

An Autolaunched Flow runs without a user-facing screen and can be invoked by other Salesforce automation, actions, Apex, or supported mechanisms.

### What is the difference between Screen Flow and Autolaunched Flow?

Screen Flow interacts with users through screens, while Autolaunched Flow runs in the background without directly presenting screens.

## Key Takeaways

- Flow Builder is the primary modern Salesforce automation tool.
- Auto-Layout is the current default Flow Builder layout.
- The + button is used to add elements in Auto-Layout.
- Get Records retrieves Salesforce data for use in the Flow.
- Flow elements perform actions and logic.
- Resources store or calculate values used by the Flow.
- Always test a Flow with Debug before activating it.
