# Task-1-festusejideaku
Repository for Task 1

# DecodeLabs Data Analytics Internship – Task 1
**Intern:** Festus Ejideaku  
**Project Milestone:** Advanced Data Cleaning & Structural Schema Enforcement  

## 📌 Business Problem
Raw transactional data frequently contains missing records, duplicate entries, and inconsistent data types that cause fatal errors when loaded into SQL databases or reporting tools. For this task, I was handed an unformatted dataset of 1,200 retail sales records that required strict structural cleaning and schema validation to establish a reliable source of truth.

## 🛠️ Technical Implementation (Power Query)
I ingested the raw transaction logs into the Power Query Editor and engineered a repeatable data cleaning pipeline:
1. **Missing Data Imputation:** Resolved systemic gaps in marketing attribution by isolating null entries in the `CouponCode` column and globally substituting them with a standardized string metric: `"NO COUPON"`.
2. **Entity Integrity Audit:** Targeted the `OrderID` column to identify and eliminate duplicate entries. This step removes redundant IDs and mathematically guarantees that every row represents an individual, unique transaction.
3. **Strict Type Casting:** Enforced hard database schema boundaries by converting alphanumeric transaction timelines to a true `Date` data type and transforming monetary values (`UnitPrice` and `TotalPrice`) strictly to `Currency` with a fixed two-decimal constraint.
