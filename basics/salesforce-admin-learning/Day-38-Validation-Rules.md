# Day 38 – Validation Rules

## What are Validation Rules?

Validation Rules maintain data quality by preventing users from saving records that do not meet defined business conditions.

If the formula evaluates to TRUE, Salesforce blocks the record and displays the error message.

## How They Work

Invalid Data → Formula = TRUE → Save Blocked → Error Message

Valid Data → Formula = FALSE → Record Saved

## Why Admins Use Them

- Prevent invalid data
- Enforce business rules
- Make fields conditionally required
- Validate numbers, dates, text, and picklist values
- Maintain consistent data quality

## Common Formula Functions

- `AND()` – All conditions must be true
- `OR()` – At least one condition must be true
- `NOT()` – Reverses TRUE/FALSE
- `ISBLANK()` – Checks whether a field is empty
- `LEN()` – Checks text length
- `ISPICKVAL()` – Checks a Picklist value
- `TODAY()` – Returns the current date
- `ISNEW()` – Checks whether a record is new
- `ISCHANGED()` – Checks whether a field changed

## Hospital Management System

Created and successfully tested 3 Validation Rules:

### 1. Doctor Experience Cannot Be Negative

`Experience < 0`

Prevents negative experience values.

### 2. Patient Age Validation

`OR(Age < 1, Age > 120)`

Ensures patient age stays within a realistic range.

### 3. Appointment Date Cannot Be in the Past

`Appointment_Date__c < TODAY()`

Prevents appointments from being scheduled for a past date.

## Important Admin Concept

A Validation Rule should normally define the invalid condition.

Example:

`LEN(Phone__c) <> 10`

If the phone number is not 10 digits, the formula returns TRUE and Salesforce blocks the save.

## Validation Rule vs Required Field

**Required Field:** Generally makes a field always required.

**Validation Rule:** Can make a field required only when a specific business condition is met.

This can require Completion Date only when the Status is Completed.

## Interview Questions

**Q: What is a Validation Rule?**  
A: A formula-based rule that prevents users from saving records containing invalid data.

**Q: When does a Validation Rule trigger an error?**  
A: When its formula evaluates to TRUE.

**Q: Can Validation Rules make a field conditionally required?**  
A: Yes. A field can be required only when another field meets a specific condition.

**Q: Do Validation Rules work only when creating records?**  
A: No. They can apply when records are created or updated.

**Q: What should an Admin test after creating a Validation Rule?**  
A: Both valid and invalid scenarios and whether the correct error message appears.
