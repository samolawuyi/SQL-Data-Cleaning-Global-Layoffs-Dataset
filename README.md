## 🔄 Project Lifecycle
**Step 1: Data Cleaning (Current Repository)** ⬅️
This stage focused on transforming raw, messy data into a standardized format.


**Step 2: [Exploratory Data Analysis (EDA)](LINK_TO_EDA_REPO)** ➡️
Once cleaned, the data was moved to the EDA stage to uncover global layoff trends and business insights.


# SQL-Data-Cleaning-Global-Layoffs-Dataset
Raw data is rarely ready for analysis. This project focuses on the end-to-end Data Cleaning and Data Transformation of a global layoffs dataset using MySQL. The goal was to take a messy raw file and create a structured, accurate, and usable dataset for future exploratory data analysis (EDA).
The 4-Stage Cleaning Process

Removing Duplicates
Identified duplicate records using Window Functions (ROW_NUMBER) partitioned across all relevant columns.

Implemented a staging table strategy to safely delete duplicate rows without risking the integrity of the original raw data.

Data Standardization
String Cleaning: Used TRIM to remove white spaces and trailing characters (e.g., fixing "United States." vs "United States").

Industry Alignment: Standardized varying industry names (e.g., merging all "Crypto", "Crypto Currency", and "CryptoCurrency" into a single category).

Date Conversion: Transformed the date column from a TEXT string to a proper DATE format using STR_TO_DATE to enable time-series analysis.

Handling Null & Blank Values
Used Self-Joins to populate missing industry data by cross-referencing records from the same company.

Applied logical updates to fill blanks where specific company information was known (e.g., mapping Airbnb to 'Travel').

Structural Refinement
Removed columns that were no longer necessary for analysis (like the helper row_num column).

Stripped out unusable data where both total_laid_off and percentage_laid_off were null, ensuring the final dataset only contains actionable insights.

Technical SQL Skills Demonstrated
DDL (Data Definition Language): CREATE TABLE, ALTER TABLE, DROP COLUMN.

DML (Data Manipulation Language): INSERT INTO, UPDATE, DELETE.

Advanced Logic: Common Table Expressions (CTEs), Window Functions, Self-Joins, and CASE statements.
