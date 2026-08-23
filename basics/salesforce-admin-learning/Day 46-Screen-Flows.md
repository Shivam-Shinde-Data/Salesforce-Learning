# Day 46 – Screen Flows

## Objective

Learn how to create a **Screen Flow** in Salesforce that allows users to enter information through a user-friendly form instead of manually creating records.

### Project Scenario

For the Hospital Management System, create a **Patient Registration Screen Flow**.

The flow allows a receptionist to enter patient information and create a new Patient record.

---

## 1. What is a Screen Flow?

A **Screen Flow** is a Salesforce Flow that displays screens to users and collects information from them.

It is useful when:

- Users need to enter information through a guided form.
- Multiple fields need to be collected at once.
- We want to simplify record creation.
- We want to provide a custom user experience.

Example:

**Receptionist → Patient Registration Screen → Enter Patient Details → Create Patient Record**

---

## 2. Create the Screen Flow

Go to:

**Setup → Flows → New Flow**

Select:

**Screen Flow**

Choose:

**Freeform**

or use the current **Auto-Layout** option if it is the default in the current Flow Builder UI.

Click **Create**.

---

## 3. Create the Patient Registration Screen

Add a **Screen** element.

Label:

`Patient Registration`

Add the following components:

### Patient Name

Component:

**Name**

Required:

**Yes**

### Age

Component:

**Number**

Label:

`Age`

Required:

**Yes**

### Phone

Component:

**Phone**

Label:

`Phone`

Required:

**Yes**

### Department

Because the Patient object contains a Lookup relationship to Department, use the current Flow Builder **Lookup** screen component.

The Lookup component requires:

- API Name
- Field API Name
- Label
- Object API Name

Example configuration:

**API Name:**
`Department_Lookup`

**Field API Name:**
`Department__c`

**Label:**
`Department`

**Object API Name:**
`Department__c`

> The Label field is only the text displayed to the user. It does not contain the Department object name. The actual Department object is specified through **Object API Name**, and the Patient's lookup relationship is specified through **Field API Name**.

If the exact API names differ in the org, use the API names shown in **Object Manager → Patient → Fields & Relationships**.

---

## 4. Important Lookup Concept

The Department field on Patient is a **Lookup Relationship**.

Therefore, the user should select an existing Department record instead of manually entering a Department name.

The Lookup component provides a searchable record-selection interface.

This is better than using a normal Text component because it maintains the relationship between:

**Patient → Department**

---

## 5. Connect the Screen

The basic flow structure is:

**Start → Patient Registration → Create Records → End**

The Screen collects the user's input.

The next element will use those screen values to create the Patient record.

---

## 6. Create the Patient Record

After the Screen element, add:

**Create Records**

Label:

`Create Patient`

Select:

**Create one record**

Object:

`Patient`

Map the screen components to Patient fields.

Example:

| Patient Field | Screen Value |
|---|---|
| Patient Name | Patient Name |
| Age | Age |
| Phone | Phone |
| Department | Department Lookup |

For the Department Lookup field, use the value returned by the Lookup component so that the Patient record stores the selected Department record ID.

---

## 7. Save the Flow

Flow Label:

`Patient Registration Flow`

API Name:

`Patient_Registration_Flow`

Save the flow.

---

## 8. Activate the Flow

After saving:

**Activate**

Only an activated flow can be used by users.

---

## 9. Test the Flow

Run the flow using **Debug** or the available flow test option.

Enter sample data such as:

- Patient Name: `Test Patient`
- Age: `45`
- Phone: `9876543210`
- Department: Select an existing Department

Finish the flow.

Then verify that a new Patient record was created.

---

## 10. Hands-On Result

Created a Screen Flow for the Hospital Management System that:

- Displays a custom Patient Registration screen.
- Collects patient information.
- Uses a Lookup component for Department selection.
- Connects the Patient to an existing Department record.
- Creates a Patient record using the collected screen values.
- Tests the flow successfully.
- Activates the flow.

---

## Interview Questions

### 1. What is a Screen Flow?

A Screen Flow is a user-interactive Flow that displays screens and collects information from users.

### 2. What is the difference between a Screen Flow and an Autolaunched Flow?

A **Screen Flow** interacts with users through screens.

An **Autolaunched Flow** runs without displaying screens and is normally started by another automation, button, Apex, or another process.

### 3. Why did we use a Lookup component for Department?

Because Department is a Lookup relationship. The user should select an existing Department record rather than manually enter a department name.

### 4. What does the Lookup component return?

It provides the selected record's value/ID, which can be used to populate the lookup field on the Patient record.

### 5. Why is a Lookup better than a Text field?

A Lookup maintains a real Salesforce relationship between records and allows users to select an existing related record.

### 6. What are the basic elements of this flow?

**Start → Screen → Create Records → End**

### 7. What happens if the Flow is saved but not activated?

Users cannot normally run the new flow version until it is activated.

### 8. Where can Screen Flows be used?

Screen Flows can be used for guided data-entry processes, registration forms, onboarding, service requests, and other user-driven business processes.

---

## Key Takeaway

Screen Flows are useful when Salesforce users need a **guided, user-friendly interface for collecting information and performing business operations**.

In our Hospital Management System, the Patient Registration Screen Flow provides a simple receptionist-friendly process:

**Enter Patient Details → Select Department → Create Patient Record**
