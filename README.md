# Healthcare Clinic Data Cleaning & Analysis

## Overview
A data cleaning and analysis project built on a 500-record healthcare clinic dataset (23 fields). The raw data was intentionally messy — simulating a real-world dataset merged from multiple hospital systems (front-desk registration, EMR, and pharmacy billing) — and required systematic cleaning before any reliable analysis could be performed.

## Tools Used
- Microsoft Excel
- Power Query (data transformation & validation)
- Pivot Tables & PivotCharts

## Process
1. **Data Quality Audit** — Identified missing values, duplicate records, inconsistent formatting, and invalid entries across the dataset.
2. **Cleaning & Standardization** — Fixed inconsistent phone number formats, invalid/malformed email addresses, mixed date formats, and inconsistent categorical values (e.g., gender, country, payment status).
3. **Duplicate Investigation** — Identified duplicate email addresses linked to different patients; cross-referenced patient names against email addresses to determine which records were likely data entry errors.
4. **Business Logic Validation** — Checked that RegistrationDate, VisitDate, and DischargeDate followed a logical sequence for every record, flagging violations.
5. **Documentation** — Logged every change and decision in a Data Cleaning Log, and compiled unresolvable issues into a separate Follow-Up table for manual review — rather than guessing or silently overwriting uncertain data.
6. **Analysis** — Built Pivot Tables and charts to extract business insights from the cleaned dataset.

## Key Findings
- Fujairah has the highest number of registered patients, with Al Ain in second place.
- Pediatrics has the highest patient volume of any department.
- Abu Dhabi generates the highest total revenue of all clinic locations — despite not having the most patients, suggesting a higher revenue per patient there.
- The patient base is fairly balanced by gender: 53% female, 47% male.
- Fractures are the most common diagnosis (43 cases), followed by conjunctivitis (37 cases).

## Files in This Repository
| File | Description |
|---|---|
| `Dirty Dataset.xlsx` | Original raw dataset before cleaning |
| `CleanData.xlsx` | Final cleaned dataset |
| `Data_Cleaning_Log_.xlsx` | Full log of every issue found and how it was handled |
| `Followup_list.xlsx` | Records flagged for manual review (unresolvable issues) |
| `Healthcare_Clinic_Data_Cleaning_Analysis.pdf` | Findings presentation |

## A Note on Approach
Not every issue in this dataset could be confidently auto-corrected. Where a fix would have required guessing (e.g., which of two patients a shared email actually belonged to, or which date in a broken sequence was wrong), the record was flagged for manual review instead of altered — reflecting how this kind of ambiguity would realistically be handled in a live business setting.
