# ApexPlanet Data Analytics Internship --- Task 1

## Data Immersion & Wrangling

This repository documents my progress on **Task 1: Data Immersion &
Wrangling** as part of the ApexPlanet Data Analytics Internship.

The objective is to understand the dataset, identify data-quality
issues, clean the data, validate the results, and prepare the dataset
for further analysis.

------------------------------------------------------------------------

## Project Overview

This project focuses on cleaning and validating a sales dataset using
Python and Pandas.

### Dataset Information

  Property               Details
  ---------------------- -----------------------------------------
  Dataset                ApexPlanet Data Analytics Dataset
  Original file          `ApexPlanet_DataAnalytics_Dataset.xlsx`
  Number of records      1,000
  Number of columns      12
  Programming language   Python
  Library                Pandas

### Columns

`Order_ID`, `Order_Date`, `Customer_ID`, `Customer_Name`, `Age`,
`Gender`, `City`, `Product`, `Category`, `Quantity`, `Unit_Price`,
`Total_Sales`

## Tools and Technologies

-   Python
-   Pandas
-   Jupyter Notebook / Google Colab
-   Microsoft Excel
-   Git and GitHub

## Data Cleaning Performed

-   Loaded the original Excel dataset using Pandas.
-   Created a copy of the original dataset before cleaning.
-   Converted `Order_Date` to datetime format.
-   Removed leading and trailing whitespace from `Gender`, `City`,
    `Product`, and `Category`.
-   Filled missing `Age` values using the median age.
-   Replaced missing `City` values with `Unknown`.
-   Saved the cleaned dataset as a CSV file.

### Missing Values

  Column            Missing Values Initially Cleaning Method
  --------------- -------------------------- -------------------------------------
  Age                                     20 Median imputation
  City                                    13 Replaced with `Unknown`
  Other columns                            0 No missing-value treatment required

After these operations, the cleaned dataset contains **1,000 rows and 12
columns, with zero remaining missing values**.

## Data Quality Checks

  -----------------------------------------------------------------------
  Validation              Result                  Status
  ----------------------- ----------------------- -----------------------
  Dataset dimensions      1,000 rows × 12 columns Completed

  Missing values after    0                       Passed
  cleaning                                        

  Exact duplicate rows    0                       Passed

  Sales calculation       0 mismatches            Passed
  consistency                                     

  Numeric range checks    No violations detected  Passed
                          under the selected      
                          rules                   

  Product--category       No inconsistencies      Passed
  consistency             detected                

  Order ID investigation  Repeated ID identified  Investigated
  -----------------------------------------------------------------------

### Order ID Investigation

The `Order_ID` value `ORD100050` appears nine times in the dataset.

Eight numeric IDs are absent from the observed range:

-   `ORD100120`
-   `ORD100240`
-   `ORD100360`
-   `ORD100480`
-   `ORD100600`
-   `ORD100720`
-   `ORD100840`
-   `ORD100960`

These missing IDs correspond to the eight additional occurrences of
`ORD100050` under the apparent sequential-ID pattern.

The intended replacements have not been confirmed. Therefore, the
original records have been preserved, and the issue has been documented
rather than automatically corrected.

## Project Files

  -----------------------------------------------------------------------
  File                                Purpose
  ----------------------------------- -----------------------------------
  `cleaned_sales_dataset.csv`         Cleaned sales dataset

  `data_quality_report.csv`           Report documenting the repeated
                                      Order ID issue

  `data_dictionary.csv`               Column descriptions, data types,
                                      and cleaning notes
  -----------------------------------------------------------------------

The cleaning code has been executed successfully in the notebook. The
reusable Python cleaning script still needs to be consolidated and
finalized.

## Current Progress

-   [x] Dataset loading and initial inspection
-   [x] Missing-value identification and treatment
-   [x] Date conversion
-   [x] Whitespace removal
-   [x] Duplicate-row check
-   [x] Sales calculation validation
-   [x] Numeric range checks
-   [x] Product--category consistency check
-   [x] Repeated Order ID investigation
-   [x] Preliminary cleaned dataset export
-   [x] Data-quality report generation
-   [x] Data dictionary generation
-   [ ] Finalize and consolidate the reusable cleaning script
-   [ ] Complete final validation and review
-   [ ] Upload all required deliverables to GitHub
-   [ ] Prepare the 3--5 minute LinkedIn project walkthrough

## Learning Outcomes

Through this task, I am developing practical skills in:

-   Data inspection and profiling
-   Missing-value handling
-   Data type conversion
-   Duplicate detection
-   Data validation
-   Data-quality documentation
-   Python-based data wrangling
-   Reproducible data-cleaning workflows

## Author

**Dhakshatha Selvaraj**

Data Analytics Intern --- ApexPlanet

------------------------------------------------------------------------

*This README reflects the project's current progress. Remaining
deliverables will be updated as the task progresses.*
