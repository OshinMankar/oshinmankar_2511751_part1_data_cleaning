# Sales Data Cleaning and Quality Assessment Project

## 1. Problem Summary

The objective of this project was to clean, validate, and prepare a sales dataset for reporting and analysis. The dataset contained issues such as missing values, inconsistent text formatting, duplicate records, invalid discounts, and date-related errors. Business rules were applied to improve data quality and generate reliable reporting outputs.

---

## 2. Dataset Description

The dataset contains sales transaction records including:

* Order Information (Order ID, Order Date, Ship Date)
* Customer Information (Customer Name, Segment, Region, State, City)
* Product Information (Category, Sub-Category)
* Sales Metrics (Quantity, Unit Price, Discount, Cost, Sales, Profit)
* Operational Information (Ship Mode, Payment Status, Order Status)

Total Records Processed: X

---

## 3. Tools Used

* Microsoft Excel
* Pivot Tables
* Excel Functions:

  * TRIM
  * SUBSTITUTE
  * COUNTIF
  * IF
  * ISNUMBER
  * YEAR
  * MONTH
  * TEXT
  * TEXTJOIN
* Conditional Validation Techniques

---

## 4. Cleaning Steps Performed

### Text Standardization

* Removed leading and trailing spaces.
* Standardized text formatting and capitalization.
* Corrected inconsistent category and sub-category values.

### Missing Value Handling

* Missing Region values replaced with "Unknown".
* Missing Ship Mode values replaced with "Unknown".
* Missing Discount values treated as 0 where applicable.

### Date Cleaning

* Converted Order Date and Ship Date to valid Excel date format.
* Identified missing and invalid dates.
* Calculated Shipping Delay Days.
* Flagged records where Ship Date occurred before Order Date.

### Duplicate Handling

* Identified exact duplicate rows.
* Identified duplicate Order IDs.
* Flagged conflicting duplicate records for review.

### Calculated Fields

* Cleaned Discount
* Calculated Sales
* Calculated Profit
* Profit Margin
* Shipping Delay Days
* Order Month
* Order Year
* Data Quality Flag

---

## 5. Business Rules Applied

* Missing Region → Filled as "Unknown".
* Missing Ship Mode → Filled as "Unknown".
* Missing Discount → Replaced with 0 where valid.
* Negative Discount → Flagged as Invalid.
* Discount Above 100% → Flagged as Invalid.
* Cancelled Orders → Excluded from completed sales summaries.
* Failed Payments → Excluded from completed sales summaries.
* Refunded Orders → Reported separately.
* Ship Date Before Order Date → Flagged as Invalid Shipping Record.

---

## 6. Summary of Data Quality Issues Found

| Issue Type                 | Count |
| -------------------------- | ----- |
| Missing Region             | 25     |
| Missing Ship Mode          | 21    |
| Missing Discount           | 18     |
| Exact Duplicate Rows       | 40     |
| Duplicate Order IDs        | 63     |
| Records Flagged for Review | 23     |
| Negative Discounts         | 10     |
| Discount Above Range       | 8     |
| Invalid Shipping Records   | 165     |
| Cancelled Orders           | 86     |
| Failed Payments            | 38     |
| Refunded Orders            | 47    |

Final Data Quality Summary:

* Clean Records: 697
* Warning Records: 32
* Invalid Records: 183
* Total Records: 912

---

## 7. Summary of Final Pivot Reports

The following pivot reports were created:

1. Sales and Profit by Region
2. Sales and Profit by Category and Sub-Category
3. Order Count by Ship Mode
4. Profit Margin by Customer Segment
5. Refunded, Cancelled, and Failed Orders by Region
6. Monthly Sales Trend

Sorting and filtering were applied to selected pivot reports for improved analysis.

---

## 8. Key Business Insights

* Certain regions generated higher sales and profit than others.
* Product performance varied significantly across categories and sub-categories.
* Customer segments showed different profitability levels.
* A portion of transactions contained data quality issues requiring review.
* Cancelled, refunded, and failed transactions impacted overall business performance.
* Monthly sales trends revealed fluctuations in revenue throughout the reporting period.

---

## 9. Assumptions and Limitations

### Assumptions

* Discount values are stored as decimal percentages.
* Valid discount range is between 0 and 1.
* Missing Region and Ship Mode values can be classified as "Unknown".

### Limitations

* Conflicting duplicate records were flagged but not manually resolved.
* Data quality checks were limited to available fields.
* Flagged records may require further business review.
* Sales calculations assume source quantity, price, and cost values are accurate.

---

## 10. Screenshots Included

The submission includes screenshots demonstrating:

* Data cleaning process
* Duplicate identification
* Date validation
* Data quality report
* Pivot table outputs
* Final reporting summaries
