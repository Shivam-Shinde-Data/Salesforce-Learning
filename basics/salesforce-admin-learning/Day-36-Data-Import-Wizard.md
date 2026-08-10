# Day 36  — Data Import Wizard

## What is Data Import Wizard?

Data Import Wizard is a Salesforce tool used to import data from CSV files into Salesforce. It is mainly useful for small-to-medium data migration tasks and supports standard objects and custom objects.

- Supports up to **50,000 records per import**
- CSV is the supported file format
- Can **Add New**, **Update Existing**, or **Add New & Update Existing** records
- Available from **Setup → Data Import Wizard**
- Supports custom objects in Developer Edition

## Import Process

1. Prepare the CSV file with correct column headers and records.
2. Go to **Setup → Data Import Wizard**.
3. Click **Launch Wizard**.
4. Select **Standard Objects** or **Custom Objects**.
5. Select the required object.
6. Choose the operation:
   - Add new records
   - Update existing records
   - Add new and update existing records
7. Select the matching method when required.
8. Upload the CSV file.
9. Select character encoding and delimiter.
10. Click **Next**.
11. Review and correct field mappings.
12. Unmapped fields will not be imported.
13. Start the import and verify the created/updated records.

## CSV Best Practices

The CSV header should match Salesforce field names as closely as possible.


Before importing:
- Check field names and data types.
- Remove unnecessary columns.
- Check for duplicate records.
- Test with a small CSV first.
- Keep a backup of important data.

## Record Matching

For custom objects, the Data Import Wizard can use:
- Record Name
- Salesforce ID
- External ID

Matching is important when updating records because it determines which existing Salesforce record should be updated.

## Important Admin Knowledge

### Data Import Wizard vs Data Loader

| Data Import Wizard | Data Loader |
|---|---|
| Up to 50,000 records | Up to 5 million records |
| Browser-based | Application |
| Simple imports | Advanced/bulk operations |
| Mainly import | Import and export |
| Easier for admins | Better for complex data migration |

Use **Data Import Wizard** for simple imports and smaller datasets. Use **Data Loader** when working with large datasets or operations such as insert, update, upsert, delete, and export.

## Permissions

For custom-object imports, the user needs appropriate object access and the **Import Custom Objects** permission. Field-level access also affects which fields can be imported.

## HMS Practice

For the Hospital Management System, I practiced importing **Department records** using a CSV file.

The Doctors import demonstrated an important real-world limitation: lookup relationships may require additional handling.

## Key Takeaways

- Data Import Wizard = simple Salesforce data import tool.
- Always prepare and validate the CSV before importing.
- Correct field mapping is essential.
- Use matching carefully when updating records.
- Test with a small dataset before a large import.
- Understand permissions before troubleshooting import errors.
- For complex lookup relationships and larger migrations, prefer Data Loader.
