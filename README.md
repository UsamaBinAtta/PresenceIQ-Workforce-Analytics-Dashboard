# PresenceIQ: Workforce Analytics Dashboard



## Employee Presence, Work-From-Home & Attendance Intelligence

PresenceIQ is an advanced HR analytics dashboard developed using **Power BI** to monitor employee attendance, workforce availability, work-from-home trends, onsite presence, and sick leave behavior.

The project transforms raw attendance records stored across multiple Excel sheets into a centralized, automated, and interactive analytics solution that helps HR teams and managers make data-driven workforce decisions.

This dashboard was designed to solve real-world HR reporting challenges in hybrid work environments where employee attendance data is distributed across multiple monthly files with inconsistent structures.

---

# Dashboard Overview

The dashboard provides a complete workforce monitoring system that enables organizations to:

- Track employee attendance performance
- Analyze work-from-home trends
- Monitor sick leave percentages
- Understand workforce availability
- Identify attendance irregularities
- Improve HR decision-making
- Automate attendance reporting

The dashboard combines data engineering, business intelligence, and HR analytics concepts into a single reporting solution.

---

# Business Problem

Many organizations store attendance records in multiple Excel sheets every month. Each sheet contains dynamic date columns such as:

| Employee Code | Name | 1-Jun | 2-Jun | 3-Jun | 4-Jun |
|---|---|---|---|---|---|
| ATQ-406 | Thanos Thakur | P | P | P | WO |
| ATQ-462 | Jarvis Singh | P | P | P | WO |

This creates several business challenges:

- Inconsistent monthly data structures
- Manual consolidation effort
- Difficulty analyzing attendance trends
- Lack of centralized workforce reporting
- No visibility into employee work preferences
- Difficulty identifying low attendance employees
- Time-consuming HR reporting processes

The organization needed a scalable reporting solution that could automate attendance analysis and provide actionable workforce insights.

---

# Solution

To address these challenges, a fully interactive Power BI dashboard was developed.

The solution includes:

- Automated data extraction from Excel files
- Data transformation using Power Query
- Dynamic attendance KPI calculations using DAX
- Interactive HR analytics dashboard
- Workforce monitoring and trend analysis
- Attendance compliance tracking
- Automated refresh using SharePoint integration

The dashboard provides real-time visibility into workforce attendance behavior and hybrid work trends.

---

# Industry / Domain

### Human Resources Analytics (HR Analytics)

This project belongs to the HR Analytics domain and focuses on workforce intelligence, attendance monitoring, and employee behavior analysis.

---

# Objectives of the Dashboard

The primary objectives of the dashboard are:

- Monitor employee attendance patterns
- Analyze work-from-home vs onsite trends
- Track sick leave percentages
- Identify employees with low attendance
- Improve workforce planning
- Reduce manual HR reporting effort
- Enable data-driven HR decisions
- Automate attendance analysis

---

# Data Source Information

## Source Type
- Microsoft Excel Files

## Source Structure

The attendance data was stored in multiple monthly Excel sheets. Each month had its own date-based columns.

Example:

| Employee Code | Name | Wed | Thu | Fri | Sat | Sun |
|---|---|---|---|---|---|---|
| ATQ-406 | Thanos Thakur | P | P | P | WO | WO |
| ATQ-462 | Jarvis Singh | P | P | P | WO | WO |

### Attendance Status Codes

| Code | Meaning |
|---|---|
| P | Present |
| WO | Weekly Off |
| WFH | Work From Home |
| SL | Sick Leave |

---

# Data Transformation Process

A major part of this project involved transforming messy attendance data into an analytical format suitable for reporting.

## Data Engineering Steps

### 1. Data Import
Imported multiple Excel sheets/files into Power BI.

### 2. Data Cleaning
Cleaned inconsistent formatting and standardized attendance records.

### 3. Data Consolidation
Combined attendance data from multiple monthly sheets into a single dataset.

### 4. Unpivot Transformation
Used the **Unpivot Columns** feature in Power Query to convert dynamic date columns into rows.

### Before Transformation

| Employee Code | 1-Jun | 2-Jun | 3-Jun |
|---|---|---|---|
| ATQ-406 | P | P | WFH |

### After Transformation

| Employee Code | Date | Status |
|---|---|---|
| ATQ-406 | 1-Jun | P |
| ATQ-406 | 2-Jun | P |
| ATQ-406 | 3-Jun | WFH |

This transformation made the dataset scalable and optimized for time-series analysis.

### 5. Data Modeling
Created relationships and structured the model for efficient reporting and DAX calculations.

---

# Dashboard KPIs

The dashboard contains several important workforce KPIs.

## Attendance KPIs

- Overall Presence Percentage
- Work From Home Percentage
- Sick Leave Percentage
- Employee Attendance Rate
- Employee WFH Rate
- Sick Leave Count
- Total Working Days
- Presence Count
- WFH Count
- Attendance Compliance Percentage

---

# Dashboard Visualizations

The dashboard contains multiple interactive visualizations.

## KPI Cards
Used for displaying:
- Presence %
- WFH %
- Sick Leave %

## Trend Charts
Used to analyze:
- Daily attendance trends
- WFH trends
- Sick leave trends

## Attendance Matrix/Table
Displays employee-level attendance information.

## Area & Line Charts
Used for:
- Workforce trend analysis
- Attendance behavior monitoring

## Interactive Slicers
Allows filtering by:
- Month
- Employee
- Attendance type

---

# Key Features

## Interactive Dashboard Experience
- Dynamic filtering
- Employee-level analysis
- Interactive attendance exploration
- Month-wise trend analysis

## Advanced Data Transformation
- Multi-sheet Excel consolidation
- Dynamic date handling
- Automated preprocessing
- Power Query transformations

## DAX-Based Calculations
Custom DAX measures were developed for:
- Presence %
- WFH %
- Sick Leave %
- Attendance counts
- Workforce KPIs

## Attendance Compliance Monitoring
The dashboard helps identify employees with attendance below the required threshold.

### Example:
- Employees with attendance below 80% can be monitored for HR action.

## Automated Refresh System
The dashboard supports:
- SharePoint folder integration
- Automatic file refresh
- Scalable monthly updates

## Workforce Insights
Provides insights into:
- Employee work preferences
- Remote work behavior
- Workforce availability
- Attendance consistency

---

# DAX Measures

Example DAX measures used in the project:

## Presence Percentage

```DAX
Presence % =
DIVIDE([Present Days], [Total Working Days])
```

## Work From Home Percentage

```DAX
WFH % =
DIVIDE([WFH Days], [Total Working Days])
```

## Sick Leave Percentage

```DAX
SL % =
DIVIDE([Sick Leave Days], [Total Working Days])
```

Additional measures were created for:
- Employee-wise analysis
- Daily attendance summaries
- Trend calculations
- Attendance compliance

---

# Dashboard Workflow

```text
Excel Attendance Files
            ↓
Power Query Data Extraction
            ↓
Data Cleaning & Transformation
            ↓
Unpivot Columns
            ↓
Data Modeling
            ↓
DAX Measure Creation
            ↓
Interactive Power BI Dashboard
```

---

# Tools & Technologies Used

| Technology | Purpose |
|---|---|
| Power BI | Dashboard Development |
| Power Query | Data Transformation |
| DAX | KPI Calculations |
| Microsoft Excel | Data Source |
| SharePoint | Automated Refresh |
| Data Modeling | Relationship Building |

---

# Business Impact

The dashboard provides several operational benefits:

- Reduced manual HR reporting effort
- Improved workforce visibility
- Faster attendance analysis
- Better workforce planning
- Improved attendance monitoring
- Hybrid work trend analysis
- Scalable reporting process

---

# Target Users

This dashboard is intended for:

- HR Teams
- Operations Managers
- Team Leads
- Workforce Planning Teams
- Senior Management

---

# Repository Structure

```text
PresenceIQ-Workforce-Analytics-Dashboard/
│
├── Dashboard/
│   ├── PresenceIQ.pbix
│
├── Dataset/
│   ├── Attendance_Data.xlsx
│
├── Screenshots/
│   ├── PresenceIQ_Dashboard.png
│
├── README.md
```

---
## Dashboard Preview

![PresenceIQ Dashboard](https://github.com/UsamaBinAtta/PresenceIQ-Workforce-Analytics-Dashboard/blob/main/PresenceIQ_Dashboard.png?raw=true)

---

# How to Run the Project

## Step 1
Download the repository.

## Step 2
Open the `.pbix` file in Power BI Desktop.

## Step 3
Update the Excel data source path if required.

## Step 4
Refresh the dataset.

## Step 5
Use filters and slicers to explore workforce insights.

---

# Future Improvements

Potential future enhancements include:

- Real-time attendance integration
- Automated email notifications
- Predictive attendance analytics
- Department-level dashboards
- AI-based workforce forecasting
- Mobile dashboard optimization
- Employee productivity scoring

---

# Learning Outcomes

This project provided practical experience in:

- Power BI Dashboard Development
- Power Query ETL Processes
- DAX Calculations
- HR Analytics
- Attendance Data Modeling
- Interactive Reporting
- Automated Reporting Solutions
- Workforce Intelligence

---

# Why This Project Matters

PresenceIQ demonstrates the ability to:

- Solve real-world business problems
- Handle messy and inconsistent datasets
- Build scalable reporting solutions
- Design interactive BI dashboards
- Perform advanced data transformations
- Create business-focused analytics solutions

This project showcases skills in both data engineering and business intelligence development.

---

# Author

## Usama Bin Atta

Data Scientist | Power BI Developer | Data Analyst

### Connect With Me

- LinkedIn: https://www.linkedin.com/in/usamabinatta/
- GitHub: https://github.com/UsamaBinAtta

---

# License

This project is created for educational, learning, and portfolio purposes.
