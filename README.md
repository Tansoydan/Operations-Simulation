# Operations Data Pipeline — Electronic Security Sector

## Overview
A commercial team at an electronic security company (CCTV, alarms, access control) 
had client data spread across three separate systems with no consolidated view of 
revenue, operational performance, or churn risk. This project consolidates those 
datasets and engineers KPI metrics to support commercial decision-making.

## Data Sources
- **Clients** — contract details, monthly fees, account managers
- **Installations** — job history, system types, engineers, costs
- **Callouts** — reactive maintenance calls, fault types, SLA response times

## What I Did
1. Audited each dataset for data quality issues — mixed date formats, inconsistent 
   casing, duplicate entries, missing values
2. Cleaned and standardised using Python and Pandas
3. Loaded into SQLite and consolidated into a single master table using SQL joins
4. Engineered KPI metrics on top of the master table
5. Exported clean dataset for Power BI dashboards

## KPIs Engineered
- Monthly and Annual Recurring Revenue (MRR/ARR) by region and contract type
- SLA breach rate overall and by region
- Repeat fault frequency per client
- At-risk client flags based on SLA breach rate and repeat fault thresholds
- Engineer callout workload and performance

## Tools
Python, Pandas, SQL (SQLite)

## Dashboard
Live Tableau dashboard: https://public.tableau.com/app/profile/taner.soydan/viz/SecurityOperationsDashboard/RevenueDash

## What This Demonstrates
- End-to-end data pipeline from raw messy inputs to clean analytical output
- Ability to identify and document data quality issues before cleaning
- SQL joins across multiple tables including subqueries to avoid row inflation
- Commercial thinking — KPIs tied directly to revenue retention and churn risk
