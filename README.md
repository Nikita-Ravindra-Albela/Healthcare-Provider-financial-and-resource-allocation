Healthcare Provider Financial & Resource Allocation Dashboard
-----------
## Overview
-----------
The Healthcare Provider Dashboard is an end-to-end Power BI analytics project designed to evaluate financial performance, insurance dependency, departmental efficiency, and patient care trends.
It combines multiple datasets to uncover actionable insights that help healthcare administrators improve cost management, service delivery, and overall operational performance. 

## I have conducted additional analysis apart from those mentioned in the problem statement.

This project highlights both technical skill (data modeling, DAX, Power Query) and business storytelling those essential for roles in data analytics and business intelligence consulting.
-----------

## Objectives
-----------
Analyze total revenue, costs, and billing efficiency across procedures and departments.

Compare insurance coverage vs. cash payments across payers.

Evaluate operational metrics such as length of stay and cost by diagnosis.

Identify demographic and regional trends driving healthcare utilization.

Support executive decisions on budgeting, staffing, and cost control.

## Datasets Used
-----------
Dataset files used -
Patients	Contains patient demographics and identifiers.
Visits	Admission, discharge, and treatment details.
Procedures	Medical and diagnostic services performed.
Departments	Organizational units within the hospital.
Diagnoses	Medical condition categories assigned to patients.
Insurance	Coverage details and payer information.
Cities / States	Geographic mapping for regional analysis.
Providers	Doctors and healthcare professionals involved.

## Data Model
-----------
Fact Table: Visits

Dimension Tables: Patients, Departments, Providers, Procedures, Diagnoses, Insurance, Cities, States

Relationships are established through keys such as:

patients[patient_id] → visits[patient_id]

departments[department_id] → visits[department_id]

insurance[insurance_id] → visits[insurance_id]

## Dashboard Pages
-----------

Page	Focus	Key Insights
1. Financial Overview	Overall revenue and cost distribution	£3M total billing, average billing £675/patient, procedure and department-level trends
2. Insurance Provider Overview	Comparison of insurance vs. cash payments	Aviva, AXA, Allianz lead in claim coverage; Hypertension & Appendicitis most covered diagnoses
3. Demographic Overview	Geographic patterns in cost and service	Edinburgh and Birmingham highest billing; Wales highest stay and cost
4. Department Overview	Departmental cost & performance analysis	Cardiology, Orthopedics, and General Surgery dominate revenue share
5. Diagnosis Overview	Disease-level financial & operational impact	Hypertension and Appendicitis show highest treatment and medication costs

## Key Metrics & DAX Measures
-----------
Measure	Description
Total Revenue = SUM(visits[billing_amount])	Total hospital billing
Total Treatment Cost = SUM(visits[treatment_cost])	Total treatment expenditure
Total Insurance Coverage = SUM(insurance[coverage_amount])	Total insured amount
Out-of-Pocket = SUM(visits[cash_payment])	Patient direct payments
Average Billing = DIVIDE([Total Revenue], COUNT(patients[patient_id]))	Avg billing per patient
Length of Stay = DATEDIFF(visits[admission_date], visits[discharge_date], DAY)	Stay duration
Gross Margin % = DIVIDE([Total Revenue]-[Total Treatment Cost],[Total Revenue])	Profitability metric


## Analytical Insights

Top 3 Revenue Departments: Cardiology (£846K), Orthopedics (£813K), General Surgery (£783K)

Top Insurance Providers: Aviva (£751K), AXA (£743K), Allianz (£731K)

Most Common Diagnoses: Hypertension, Appendicitis, Asthma

Average Stay Duration: 4.87 days, with maximum 9 days in complex cases

High-Cost States: Wales and Northern Ireland show above-average treatment costs

## Business Value

Enables cost-to-care ratio analysis for each department.

Identifies high-performing insurance providers and patient demographics.

Assists in budget forecasting and revenue optimization.

Serves as a base for predictive modeling (e.g., future revenue or LOS forecasts).

Builds transparency between financial, clinical, and administrative units.

## Tools & Techniques

Power BI – Data modeling, DAX, and visualization

Power Query – ETL and data transformation

Excel / CSV Files – Base datasets

Map, KPI, Waterfall, and Matrix visuals – Dynamic visuals for clarity

Slicers (City, State, Department, Date) – Fully synced for cross-page filtering

## Project Highlights

✅ End-to-end ETL + modeling + analysis
✅ Professionally structured KPI layer
✅ Interactive maps and department comparisons
✅ Insight-driven storytelling design
✅ Real-world healthcare context (finance, insurance, operations)


## Author

Nikita Ravindra Albela
Data Analyst | Power BI Developer | Business Intelligence Enthusiast
nikitaalbela31@gmail.com
GitHub Profile 


 Suggested Repository Structure
 Healthcare-Provider-Dashboard
 Healthcare Provider Dashboard.pbix
 Data/
 patients.csv
 visits.csv
 diagnoses.csv
 departments.csv
 insurance.csv
 procedures.csv
 Screenshots/
 README.md
