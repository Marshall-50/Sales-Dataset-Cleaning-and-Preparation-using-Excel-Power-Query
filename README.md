
![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/cover2.jfif)
# Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query

## Introduction

In today's data-driven world, the journey to valuable insights begins with clean, reliable data. As part of the #datachallengewithIfunanyaGabriel, I took on the task of transforming a disorganized and error-prone sales dataset into a structured, analysis-ready format using Power Query in Microsoft Excel.

This project mirrors the kind of challenges data analysts face in real business environment: inconsistent formats, invalid entries, merged fields, and non-numeric values hidden behind text. 
My goal was to demonstrate not only technical proficiency but also a logical, step-by-step approach to identifying and resolving data quality issues.

Through this hands-on challenge, I reinforced essential data cleaning skills and developed a repeatable process that can be scaled and reused. The result is a well-documented, reproducible pipeline that prepares the data for meaningful analysis and reporting.
This project reflects my attention to detail, my ability to solve real-world data problems, and my commitment to delivering clean, trustworthy data, a core foundation for any data analyst.

## Overview of the Project
The dataset contained two batches of raw sales records from a fictional company. It included customer details, order info, sales amounts, shipping modes, and locations.

The data was messy and inconsistent, just like the kind of raw data analysts receive in real business scenarios. My goal was to transform this chaotic dataset into a clean, structured version ready for insightful analysis.

![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/Screenshot%20(39).png)
![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/Screenshot%20(38).png)
##  Skills Demonstrated

- Data cleaning and wrangling  
- Data transformation using Power Query  
- Handling missing and invalid values  
- Text standardization and formatting  
- Data type conversion  
- Splitting and merging columns  
- Removing duplicates and unnecessary rows  
- Combining multiple datasets  
- Applying conditional logic  
- Building reproducible data pipelines  
- Data quality assessment and assurance  
- Preparing data for analysis

  ## Data Issues Identified

The dataset had multiple real-world quality issues, including:

-  Two separate data sources (Batch 1 and Batch 2)
-  Merged fields: `Customer Name` and `Customer ID` were combined in one column
-  Invalid entries in the `Order Date` column (e.g., "invalid date")
-  Currency symbols in the `Sales` column (`₦`, `$`)
-  Worded numbers (e.g., "five", "three") in the `Quantity` column
-  Inconsistent state names (abbreviations, lowercase, extra spaces)
-  Mixed casing and formatting in the `Ship Mode` column
-  Missing values in key columns (e.g., `Order ID`, `Sales`)
-  Duplicate records

## 🔄 Power Query Cleaning Process

Here’s a step-by-step breakdown of how I cleaned the dataset using Power Query:

### 1️⃣ Combine Both Batches
- Loaded Batch 1 and Batch 2 into Power Query.
- Used **Append Queries** to merge the two tables into a unified dataset called **Combined Data**


  ![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/append.png)

### 2️⃣ Split Combined Customer Column
- Split the `Customer Info` column into `Customer Name` and `Customer ID` using `Split Column by Delimiter`.

![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/split%20colun.png)

### 3️⃣ Clean and Standardize Dates
- Replaced text like "invalid date" with nulls.
- Converted the `Order Date` column to a valid **Date** format.
- Removed rows with null dates.
- Replace null dates with 1/31/2021 and flagged it for review using Conditional Formatting

### 4️⃣ Convert Worded Quantities
- Replaced values like "five", "three", etc., with numeric values using **Conditional Column** logic.

### 5️⃣ Standardize Categorical Columns
- Standardize casing in `State` and `Ship Mode`. Replace empty cells with "Unknown". Then Flagged it for Review using Conditional formatting
- Replaced state abbreviations (e.g., "calif.") with full names using Replace value
- Removed leading and trailing spaces using **Trim**.
- Created a new column for Product Category using Conditional Column and arrange product category with its rightful product Name.


![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/conditonal%20colunm.png)

### 6️⃣ Clean the Sales Column
- Removed currency symbols using **Replace Values**.
- Converted the column to **whole numbers** for calculations.
  
### 7️⃣ Remove Nulls and Duplicates
- Filtered out rows missing key fields (`Order ID`, `Customer Name`, `Sales`, `Date`, `Quantity`).
- Removed exact duplicate rows using **Remove Duplicates**.

### 8️⃣ Enforce Correct Data Types
- Verified all columns had the correct data type (Text, Number, or Date).

![](https://github.com/Marshall-50/Sales-Dataset-Cleaning-and-Preparation-using-Excel-Power-Query/blob/main/ready.png)


The cleaned dataset is now:
- Structured and analysis-ready
- Free from critical errors and duplicates
- Easy to refresh and audit thanks to Power Query’s step history


## Final Thoughts

Cleaning data is a **critical part of the data analytics workflow**. With Power Query, I didn’t just clean the data — I built a transparent and repeatable pipeline.

### This project highlights my ability to:
- Handle messy, unstructured real-world data
- Use Power Query for scalable, automated data transformations
- Prepare data for meaningful insights and analysis

Thank You for Reading

Connect With Me

[LinkedIn](https://www.linkedin.com/in/marshallufomba/)
