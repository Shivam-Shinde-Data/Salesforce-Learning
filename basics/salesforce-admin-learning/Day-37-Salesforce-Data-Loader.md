# Day 37 — Salesforce Data Loader

## What is Data Loader?
Data Loader is a Salesforce client application used for bulk data operations.

## Main Operations
- Insert — Add new records
- Update — Modify existing records
- Upsert — Update existing records and insert new ones
- Delete — Delete records
- Export — Export Salesforce records
- Export All — Export records including deleted records

## Data Loader vs Import Wizard
- Import Wizard — Simple, browser-based, suitable for smaller/simple imports
- Data Loader — More powerful, suitable for larger data operations and supports Insert, Update, Upsert, Delete and Export

## Important Concepts
- Data Loader commonly uses CSV files.
- CSV columns are mapped to Salesforce fields.
- Record ID is commonly used to identify records for Update and Delete.
- After an operation, success and error files show which records succeeded or failed.
- Error files help identify issues such as invalid values, missing required fields, incorrect IDs or permission problems.

## Interview Questions

Q: What is Data Loader?
A: A Salesforce client application used for bulk data operations such as Insert, Update, Upsert, Delete and Export.

Q: What is Upsert?
A: Upsert combines Update and Insert. Existing records are updated and records that do not exist are inserted.

Q: When would you use Data Loader instead of Import Wizard?
A: When larger data volumes or advanced operations such as Update, Upsert, Delete or Export are required.

Q: What file format does Data Loader commonly use?
A: CSV.
