# Healthcare Pharma Analytics Dashboard

Tools: Excel, Power Query, PivotTables, PivotCharts, Slicers
Rows: 48,624 hospital visits | 30 columns

## What this project shows
The source file looked complete, but the dates were not usable. Admission and discharge dates were stored in four formats, and most calculated stays were impossible. The dashboard reports both the business metrics and that data-quality problem.

## Cleaning in Power Query
- Standardized gender to Male, Female, and Divers
- Standardized blood type, discharge status, and payment status
- Replaced blank medications and the text NULL with Not recorded
- Parsed mixed dates into real date columns: yyyy-MM-dd, dd-MM-yyyy, dd/MM/yyyy, MM/dd/yyyy, and dd MMM yyyy
- Calculated Age at Admission and Length of Stay from the cleaned dates
- Flagged bad date rows instead of deleting them

## Data-quality result
| Date flag | Rows |
|---|---:|
| Discharge before admission | 24,215 |
| Stay over 60 days | 22,367 |
| Valid stay (0–60 days) | 2,007 |
| Age out of range | 35 |

The original length_of_stay_days field was already between 0 and 60 on every row, so stay KPIs use that field. The calculated stay is used only to show that the raw dates cannot be trusted.

## Dashboard
- KPI cards: total patients, total charges (EUR), average charge, average length of stay, readmission rate, valid date rows
- Patients by department
- Charges by insurance provider
- Patients by primary diagnosis
- Payment status and discharge status
- Date-quality chart
- Slicers: department, insurance, payment status, discharge status, gender, diagnosis

## Skills
Power Query, data cleaning, date parsing, PivotTables, KPI design, Excel dashboard layout, data-quality reporting

## Author
Oladotun Ajayi
https://www.linkedin.com/in/dotunajayi
