Data Immersion and Wrangling – Sales Dataset

1. Project Overview
This project focuses on exploring, assessing, cleaning, and transforming a sales dataset to prepare it for further analysis. The objective is to identify data quality issues, apply appropriate cleaning techniques, and generate a reliable analysis-ready dataset.

3. Tools and Technologies
- Python
- Pandas
- Microsoft Excel
- Google Colab
  
3. Dataset Description
The dataset contains 1,000 sales records and 12 attributes covering order details, customer information, product categories, quantities, pricing, and sales amounts.
Attribute	Description
Order_ID	Order identifier
Order_Date	Date of the order
Customer_ID	Customer identifier
Customer_Name	Customer name
Age	Customer age
Gender	Customer gender
City	Customer location
Product	Purchased product
Category	Product category
Quantity	Number of units purchased
Unit_Price	Price per unit
Total_Sales	Total sales amount

4. Data Quality Assessment
An initial assessment was performed to identify missing values, duplicate records, inconsistent formatting, and potential anomalies.
Data Quality Check	Finding
Total records	1,000
Total columns	12
Missing Age values	20
Missing City values	13
Exact duplicate rows	0
Repeated Order_ID	ORD100050 (9 occurrences)

5. Data Cleaning and Transformation
The following operations were performed:
- Date standardization: Converted the Order_Date column into a consistent datetime format.
- Missing Age values: Replaced missing values using the median age.
- Missing City values: Replaced missing entries with Unknown.
- Text standardization: Removed leading and trailing whitespace from categorical columns.
- Duplicate assessment: Checked for exact duplicate records.
- Order ID investigation: Identified repeated order identifiers and retained the records because the intended replacement identifiers could not be confirmed.
6. Cleaned Dataset Generation
After completing the cleaning operations, the processed dataset was exported as:

cleaned_sales_dataset.csv

The CSV file was generated without including the DataFrame index.

7. Validation and Results
The cleaned dataset was reloaded and checked to verify the cleaning results.
Validation	Result
Final records	1,000
Final columns	12
Remaining missing values	0
Exact duplicate rows	0
Invalid age values	0
Non-positive quantities	0
Non-positive unit prices	0
Non-positive sales values	0
Sales calculation mismatches	0

The sales calculation was validated against the relationship between quantity and unit price.

9. Conclusion
The sales dataset was successfully explored, assessed, cleaned, and transformed into an analysis-ready CSV file. Missing values were handled, categorical text was standardized, and validation checks were performed to assess data consistency.

The repeated Order ID anomaly was documented without making unsupported changes to the original records.
