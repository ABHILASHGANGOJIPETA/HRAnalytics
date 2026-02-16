# HR Presence Insights Dashboard (Power BI)

## Project Overview

This project analyzes employee attendance data to understand work patterns in a hybrid work environment. The goal was to transform multiple raw Excel attendance sheets into a clean analytical dataset and build an interactive Power BI dashboard that helps HR teams monitor attendance, work‑from‑home behavior, and sick leave trends.

The solution automates data cleaning, standardizes monthly files, and provides actionable insights for workforce planning and decision making.

---

## Business Problem

The HR team stored attendance records across multiple Excel files (monthly sheets) with inconsistent formats and date columns. Because of this, they could not:

* Track attendance percentage accurately
* Identify work‑from‑home preferences
* Monitor sick leave patterns
* Understand weekly employee behavior

Manual analysis in Excel was time‑consuming and error‑prone.

---

## Objective

Build a dynamic dashboard that:

* Combines multiple monthly files automatically
* Cleans and standardizes attendance data
* Calculates attendance metrics
* Visualizes employee behavior trends
* Supports hybrid work planning decisions

---

## Tools & Technologies

* Power BI
* Power Query (ETL & Data Transformation)
* DAX (Data Analysis Expressions)
* Excel (Raw Data Source)

---

## Data Processing (ETL)

The dataset contained three months of attendance sheets where each day existed as a separate column.

### Key Transformations

1. Removed metadata rows
2. Promoted first row as headers
3. Standardized column names
4. Converted data types
5. Unpivoted date columns into Date–Status format
6. Created reusable Power Query function
7. Applied function to all monthly sheets
8. Appended into a single fact table

This created a scalable pipeline — new monthly files can be added without modifying queries.

---

## Data Model & Calculations

### Custom Column

**WFH Count Logic**

* Present (P) = 1
* Work From Home (WFH) = 1
* Half WFH (HWFH) = 0.5
* Leave = 0

### DAX Measures

* Total Working Days (excluding weekends & holidays)
* Present Days
* Attendance %
* Work From Home %
* Sick Leave %

---

## Dashboard Features

* KPI cards for Attendance %, WFH %, Sick Leave %
* Attendance trend over time
* WFH trend analysis
* Sick leave trend analysis
* Day‑of‑week behavior analysis
* Employee‑level attendance table
* Monthly filtering & date slicers

---

## Key Insights

* Average attendance remained around 91–93%
* WFH highest on Mondays and Fridays
* Mid‑week shows highest office presence
* Sick leave spike observed mid‑month (possible seasonal trend)

---

## Business Impact

The dashboard helped HR to:

* Plan office seating capacity
* Schedule meetings on optimal days
* Monitor abnormal leave spikes
* Understand hybrid work behavior
* Replace manual Excel analysis with automated reporting

---
## How to Use

1. Download the PBIX file
2. Open in Power BI Desktop
3. Replace or add new monthly Excel files in the data folder
4. Refresh the dataset
5. Dashboard updates automatically

---

## Future Improvements

* Connect to SharePoint or database for auto refresh
* Add department‑level analysis
* Add employee performance correlation

---

## Author

Abhilash Gangojipeta
Data Analytics Enthusiast | Power BI | Excel | SQL
