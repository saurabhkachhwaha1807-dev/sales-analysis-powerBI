# Sales Analysis

This exercise focuses on data preparation, transformation, and visualization using Power BI and DAX. The business context involves managing and relating multiple tables of retail data from four disparate files to eventually create a high-level dashboard

### 🎯 Objective and Context

**Objective:** Load data from multiple sources, define and manage relationships, and enhance the dataset using DAX syntax to prepare for dashboard creation.
Data Source: Retail data provided in 4 separate files.

### 🛠️ Required Tasks

**Data Loading and Cleaning** 

**Load Data:** Load all four files into the data model, ensuring the header contains the field names.

**Data Cleaning:**

* Drop records from the 'PinCode-Geo' table where 'Zone' is missing.
* Drop records from 'Mod3_Raw_CityTier_v0 1' where 'CityTier' is missing.

**Relationships:** Define relationships for common columns between tables. Specifically, create a relationship between the 'City' field in 'Mod3_Raw_CityTier_v0 1' and the 'City' field in the 'PinCode-Geo' table

**Required Actions** (The Work Done)

* The initial phase involved Data Loading and Cleaning to establish a robust data model:
* File Loading and Setup: All four disparate data files were loaded into the data model, ensuring correct field names from the headers.

**Data Quality Enforcement:** Missing values were removed from key tables:
* Records in 'PinCode-Geo' with missing 'Zone' values were dropped.
* Records in 'Mod3_Raw_CityTier_v0 1' with missing 'CityTier' values were dropped.

**Relationship Management:**  Relationships were established for common columns across tables, critically connecting the 'City' field between 'Mod3_Raw_CityTier_v0 1' and 'PinCode-Geo', and finally updating all relationships to ensure a fully connected model.
* The subsequent phase focused on Data Enhancement and Transformation using DAX:

**Metric Calculation:** A core measure, 'Net_Units', was created in the sale table by calculating the difference between 'Units' and 'Cancelled Units'.

**Geographical Standardization:**  The 'City' field in two files ('Mod3_Raw_CityTier_v0 1' and 'PinCode-Geo') was standardized by
Renaming the original column to 'City_Old'.
* Creating a new column named 'City' containing only the city name, with the country part removed.

**Time Intelligence:** Two new fields were created to enable time-based analysis:
* 'OrderDayOfWeek': Provided the full name of the day of the week (e.g., 'Monday').
* 'OrderWeekStart': Calculated the date of the start of the week (starting Monday) and was formatted to display concisely (e.g., 'Nov 06').
