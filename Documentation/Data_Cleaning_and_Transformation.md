# 🧹 Data Cleaning & Transformation

## 📌 Overview

The raw **HR Analytics dataset** was imported from **Microsoft Excel into Microsoft Power BI**, where data cleaning and transformation were performed using **Power Query**.

The original Excel file was preserved as the **raw source dataset**, while the data preparation and transformation steps were performed within Power BI to create an analysis-ready dataset for dashboard development.

---

## 📂 Source Dataset

| Attribute | Details |
|---|---|
| **Source** | Microsoft Excel |
| **Dataset** | HR Analytics |
| **Raw Records** | 5,000 rows |
| **Raw Columns** | 37 columns |
| **Transformation Tool** | Power Query |
| **Visualization Tool** | Microsoft Power BI |

The dataset contains employee-level HR information covering demographic, job, compensation, satisfaction, and employment-related attributes.

### Key Fields

- Employee ID
- Age
- Attrition
- Business Travel
- Department
- Job Role
- Job Satisfaction
- Salary Slab
- Years of Experience
- Gender
- Overtime
- Work-Life Balance
- Job Involvement
- Current Role Tenure
- Number of Companies Worked
- And other HR-related attributes

---

## 🔄 Power Query Transformation Process

The following transformations were applied to prepare the raw dataset for analysis.

### 1. Source

The raw HR dataset was connected to Power BI using the original Excel workbook.

The Excel file was retained separately as the raw source to preserve the original data.

### 2. Navigation

The required **`HR_Analytics`** sheet/table was selected from the Excel workbook for further processing.

### 3. Promoted Headers

The appropriate row was promoted to become the column headers.

This ensured that each field was correctly identified and structured for subsequent transformations.

### 4. Changed Type

Appropriate data types were assigned to the relevant columns.

This included validating:

- Numeric fields
- Text fields
- Categorical fields
- Date-related fields where applicable

Correct data types ensure that calculations, filtering, sorting, and visualizations work as expected.

### 5. Sorted Rows

The dataset was sorted as part of the data preparation workflow to organize the records appropriately.

### 6. Removed Top Rows

Unnecessary rows from the beginning of the source data were removed to ensure that only relevant employee records remained in the dataset.

### 7. Removed Duplicates

Duplicate records were removed to prevent repeated employee records from affecting employee-level analysis and dashboard metrics.

### 8. Filtered Rows

Rows were filtered where required to retain records relevant to the HR analysis.

This helped ensure that the final dataset contained appropriate records for dashboard reporting.

### 9. Replaced Values

Selected values were replaced where required to maintain consistency across categorical fields and improve data quality.

### 10. Changed Type1

After the preceding transformations, data types were reviewed and adjusted again where necessary.

This final validation ensured that the transformed dataset remained correctly formatted before analysis.

---

## 🔢 Creating the `AttritionCount` Column

A conditional column named **`AttritionCount`** was created in Power Query to convert the categorical `Attrition` field into a numeric indicator.

### Logic

    If Attrition = "Yes" → 1
    If Attrition = "No"  → 0

### Example

| Attrition | AttritionCount |
|---|---:|
| Yes | 1 |
| No | 0 |

The `AttritionCount` column makes employee attrition easier to aggregate and analyze in Power BI.

---

## 📊 Data Preparation Outcome

After applying the Power Query transformations, the dataset was prepared as an **analysis-ready dataset** for Power BI reporting and visualization.

The prepared data supports analysis of:

- Employee attrition
- Department-wise employee distribution
- Salary slab-wise attrition
- Age group analysis
- Gender-wise attrition
- Job role analysis
- Job satisfaction
- Employee experience
- Overtime
- Work-life balance
- Job involvement
- Current role tenure
- Number of companies worked

---

## 📈 Dashboard Metrics

The transformed dataset was used to develop the **HR Analytics Dashboard** and calculate key workforce and attrition metrics.

### Key KPIs

| KPI | Value |
|---|---:|
| **Total Employees** | **4,937** |
| **Active Employees** | **4,098** |
| **Attrition Count** | **839** |
| **Attrition Rate** | **16.99%** |
| **Average Age** | **37** |
| **Average Experience** | **6.47 Years** |

### Additional Metrics

| Metric | Value |
|---|---:|
| **Average Income** | **48.92K** |
| **Average Companies Worked** | **2.63** |
| **Average Distance** | **9.69** |
| **Average Role Tenure** | **3.84 Years** |

### Interactive Filters

The dashboard allows users to dynamically explore employee segments using:

- **Age Group**
- **Department**
- **Over Time** *(Deep Dive page)*

---

## 🧮 DAX & Analysis

After completing the Power Query transformation process, **DAX measures** were used within Power BI to calculate key HR metrics and support interactive analysis.

The prepared dataset and DAX measures together enabled the creation of dynamic KPIs and visualizations for employee attrition and workforce analysis.

---

## 🔄 Data Preparation Flow

    Raw Excel Dataset (5,000 Rows × 37 Columns)
           ↓
    Import into Power BI
           ↓
    Power Query
           ↓
    Promote Headers
           ↓
    Change Data Types
           ↓
    Sort Rows
           ↓
    Remove Unnecessary Rows
           ↓
    Remove Duplicates
           ↓
    Filter Rows
           ↓
    Replace Values
           ↓
    Review Data Types
           ↓
    Create AttritionCount
           ↓
    Analysis-Ready Dataset
           ↓
    DAX Measures & Calculations
           ↓
    HR Analytics Dashboard

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Raw HR dataset and source data |
| **Microsoft Power BI** | Data modeling, dashboard development, and visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Measures, KPIs, and analytical calculations |

---

## 🎯 Objective of Data Preparation

The primary objective of the data preparation process was to:

- Improve data consistency
- Remove unnecessary and duplicate records
- Ensure correct data types
- Standardize relevant values
- Create calculated indicators required for analysis
- Prepare a reliable dataset for Power BI reporting

This transformation process provides a structured foundation for building interactive HR analytics and employee attrition dashboards.

---

## 📝 Summary

The original **5,000-row, 37-column HR dataset** was preserved in **Microsoft Excel** as the raw source file.

All major data cleaning and transformation activities were performed using **Power Query within Microsoft Power BI**. The transformed dataset was then combined with **DAX measures** to develop an interactive HR Analytics Dashboard.

This workflow demonstrates an end-to-end data preparation process:

**Raw Data → Data Cleaning → Transformation → Analysis → Visualization**

The resulting dataset supports interactive KPI reporting and multidimensional analysis of employee attrition and workforce characteristics.