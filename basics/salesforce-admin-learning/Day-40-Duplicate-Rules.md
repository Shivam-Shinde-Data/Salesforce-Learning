# Day 40 — Duplicate Rules

## What I Learned

Duplicate Rules in Salesforce help identify records that may already exist and prevent or warn users about duplicate data.

### Duplicate Rule vs Matching Rule

- **Matching Rule:** Defines how Salesforce identifies duplicates.
- **Duplicate Rule:** Defines what Salesforce should do when a duplicate is detected.

**Flow:**
`Matching Rule → Identifies Duplicate → Duplicate Rule → Takes Action`

## Hands-On: Patient Duplicate Phone Rule

Created a Duplicate Rule for the **Patient** object to identify patients with the same phone number.

### Matching Rule
- **Name:** `Patient_Phone_Matching`
- **Object:** Patient
- **Field:** Phone
- **Matching Method:** Exact
- **Match Blank Fields:** Disabled

### Duplicate Rule
- **Name:** `Patient_Duplicate_Phone`
- **Compare Patients With:** Patients
- **Action on Create:** Allow + Alert + Report
- **Action on Edit:** Allow + Alert
- **Conditions:** None

The rule displays a warning when a Patient with the same phone number already exists, while still allowing the record to be saved.

## Key Takeaways

- Matching Rules decide **what counts as a duplicate**.
- Duplicate Rules decide **what happens after a duplicate is detected**.
- `Exact` matching is useful for fields such as phone numbers.
- Duplicate Rules can **Alert, Report, or Block** duplicate records.
- Duplicate management is important for maintaining clean and reliable Salesforce data.

## Result

Successfully created and tested a Patient duplicate rule based on the **Phone** field.
