# Day 51 – Record-Triggered Flow

## Objective

Learn how to create a **Record-Triggered Flow** in Salesforce that automatically performs an action when a record is created or updated.

### Project Scenario

For the Hospital Management System, create a **Patient Follow-Up Flow**.

When a new Patient record is created, the flow automatically creates a Task for follow-up.

---

## 1. What is a Record-Triggered Flow?

A **Record-Triggered Flow** automatically runs when a Salesforce record is created, updated, or deleted, depending on the configured trigger.

It is useful when:

- Automation should happen automatically after a record change.
- Users should not need to manually start the process.
- Related records or actions need to be created or updated.

Example:

**Patient Created → Record-Triggered Flow → Create Follow-Up Task**

---

## 2. Create the Record-Triggered Flow

Go to:

**Setup → Flows → New Flow**

Select:

**Record-Triggered Flow**

Click **Create**.

---

## 3. Configure the Start Element

Configure the flow to run when a Patient record is created.

Example configuration:

**Object:** `Patient`

**Trigger:** A record is created

**Entry Conditions:** Use the required Patient conditions for the automation.

For this project, the flow should run for newly created Patient records.

---

## 4. Choose Flow Optimization

Choose:

**Actions and Related Records**

This option is used when the flow needs to perform actions after the triggering record is saved.

Examples:

- Create related records
- Update related records
- Create Tasks
- Send notifications
- Perform other actions

For our Patient automation, this is required because the flow creates a **Task**.

---

## 5. Create the Follow-Up Task

Add a **Create Records** element.

Label:

`Create Follow-Up Task`

Select:

**Create one record**

Object:

`Task`

Set the required Task field values.

Example:

| **Task Field** | **Value** |
|---|---|
| Subject | Patient Follow-Up |
| Status | Not Started |
| Priority | Normal |
| Related To | Triggering Patient Record |

The **Related To** field should reference the Patient record that triggered the flow.

---

## 6. Flow Structure

The basic flow structure is:

**Patient Created → Create Follow-Up Task → End**

The `$Record` global variable represents the record that triggered the flow.

---

## 7. Save and Activate the Flow

Flow Label:

`Patient Follow-Up Flow`

API Name:

`Patient_Follow_Up_Flow`

Save the flow.

After saving, click **Activate**.

Only the activated version will run automatically when the configured trigger occurs.

---

## 8. Test the Flow

Create a new Patient record.

Example:

- Patient Name: `Test Patient`
- Age: `45`
- Phone: `9876543210`

After saving the Patient record, verify that a new **Task** has been created and is related to that Patient.

---

## 9. Before-Save vs After-Save Flow

### Fast Field Updates

Used mainly to update fields on the triggering record before it is saved.

Example:

**Patient Created → Automatically Set a Field Value**

### Actions and Related Records

Used when the flow needs to perform actions after the record is saved.

Example:

**Patient Created → Create Task**

For this project, we used **Actions and Related Records**.

---

## 10. Hands-On Result

Created a Record-Triggered Flow for the Hospital Management System that:

- Runs automatically when a Patient record is created.
- Uses **Actions and Related Records**.
- Creates a follow-up Task automatically.
- Relates the Task to the triggering Patient record.
- Tests the automation successfully.
- Activates the flow.

---

## Interview Questions

### 1. What is a Record-Triggered Flow?

A Record-Triggered Flow is a flow that automatically runs when a record is created, updated, or deleted according to its configured trigger.

### 2. What are the main optimization options?

The main options are **Fast Field Updates** and **Actions and Related Records**.

### 3. When should you use Fast Field Updates?

When you need to update fields on the triggering record before it is saved.

### 4. When should you use Actions and Related Records?

When the flow needs to create or update related records or perform actions after the triggering record is saved.

### 5. What is `$Record` in a Record-Triggered Flow?

`$Record` is a global variable that represents the record that triggered the flow.

### 6. Can a Record-Triggered Flow create a Task?

Yes. A Record-Triggered Flow can use **Create Records** to automatically create a Task.

### 7. What is the difference between a Screen Flow and a Record-Triggered Flow?

A **Screen Flow** interacts with users through screens, while a **Record-Triggered Flow** runs automatically when a configured record change occurs.

### 8. Why did we use Actions and Related Records?

Because our automation creates a separate **Task** record after the Patient record is saved.

---

## Key Takeaway

Record-Triggered Flows are used to automate Salesforce processes based on record changes.

In our Hospital Management System:

**Create Patient → Flow Runs Automatically → Follow-Up Task Created**
