# Day 39 – Formula Fields

## What is a Formula Field?

A Formula Field is a **read-only field** that automatically calculates a value using other Salesforce fields and formulas.

The value is calculated dynamically, so when the source field changes, the Formula Field updates automatically.

## Formula Field vs Validation Rule

- **Formula Field:** Calculates and displays information.
- **Validation Rule:** Prevents invalid data from being saved.

## Hospital Management System

Created and tested a Formula Field on the **Doctors** object:

### Experience Category

Purpose: Automatically categorizes doctors based on their years of experience.

Formula:

`IF(Experience < 3, "Fresher", IF(Experience < 8, "Experienced", "Senior"))`

Categories:

- 0–2 years → Fresher
- 3–7 years → Experienced
- 8+ years → Senior

Example:

`Experience = 12 → Experience Category = Senior`

If Experience changes to 5, the Formula Field automatically changes to **Experienced**.

## Important Formula Functions

Common functions used in Formula Fields:

- `IF()` – Conditional logic
- `AND()` – All conditions must be true
- `OR()` – At least one condition must be true
- `TODAY()` – Current date
- `TEXT()` – Converts values to text
- `ISBLANK()` – Checks whether a field is empty

## Key Admin Points

- Formula Fields are read-only.
- Users cannot manually enter their values.
- Values are calculated automatically.
- They can be used for calculations, categorization, dates, text, and business logic.
- Formula Fields can reference other fields and supported related-object fields.

## Interview Questions

**Q: What is a Formula Field?**  
A: A read-only field that automatically calculates a value using a Salesforce formula.

**Q: Can users edit a Formula Field?**  
A: No, the value is calculated automatically.

**Q: What happens when the source field changes?**  
A: The Formula Field automatically recalculates.

**Q: Formula Field vs Validation Rule?**  
A: Formula Fields calculate or display information, while Validation Rules prevent invalid records from being saved.
