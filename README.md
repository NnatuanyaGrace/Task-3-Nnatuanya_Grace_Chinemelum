# E-commerce Data Analysis Using SQL Server

## Project Overview

This project analyses e-commerce order data using Microsoft SQL Server to evaluate order statuses, product performance, payment methods, yearly sales trends, and data quality.

The objective is to demonstrate how SQL can be used to extract meaningful insights from transactional data, identify business patterns, and support data-driven decision-making.

## Tools and Technologies

* **Database:** Microsoft SQL Server
* **Query Tool:** SQL Server Management Studio (SSMS)
* **Language:** SQL
* **Dataset:** E-commerce Orders Dataset

## Business Questions

The analysis was designed to answer the following business questions:

1. How many orders were delivered, shipped, cancelled, returned, and pending?
2. Which orders had the highest total prices?
3. What orders were recorded in 2024?
4. Which products generated the highest recorded sales value?
5. Which products had the highest total quantity sold?
6. How did products compare in order frequency, quantity sold, average unit price, and recorded sales value?
7. Which payment methods were most frequently recorded?
8. How did unique order counts and recorded sales values vary by year?
9. Were there missing values in selected important columns?

## SQL Skills Demonstrated

This project demonstrates the practical application of the following SQL concepts:

* `SELECT` and `TOP` for retrieving records and limiting results.
* `WHERE` for filtering data based on specified conditions.
* `ORDER BY` for sorting query results.
* `GROUP BY` for summarizing data across categories.
* `COUNT()` for counting records.
* `COUNT(DISTINCT)` for counting unique, non-NULL order IDs.
* `SUM()` for calculating totals.
* `AVG()` for calculating averages.
* `CASE WHEN` for conditional counting.
* `YEAR()` for extracting years from dates.
* `IS NULL` for checking missing values.

##  Analysis Performed

### Order Status Analysis

Counted orders across five statuses: Delivered, Shipped, Cancelled, Returned, and Pending.

**Results:**

| Order Status | Number of Orders | Percentage |
| ------------ | ---------------: | ---------: |
| Cancelled    |              250 |     20.83% |
| Returned     |              247 |     20.58% |
| Pending      |              237 |     19.75% |
| Shipped      |              235 |     19.58% |
| Delivered    |              231 |     19.25% |
| **Total**    |        **1,200** |   **100%** |

**Key Insight:**

Cancelled orders were the most frequently recorded status, accounting for 250 orders (20.83%). Returned orders followed with 247 orders (20.58%).

Together, cancelled and returned orders accounted for 497 records, representing 41.42% of the total.

### High-Value Order Analysis

Filtered orders with a `TotalPrice` greater than 1,000 and sorted them in descending order to identify the five highest-value records among the qualifying orders.

**SQL concepts applied:** `SELECT`, `TOP`, `WHERE`, and `ORDER BY`.

**Business relevance:** This analysis provides a way to identify high-value order records and examine their associated products and quantities.

### Date-Based Analysis

Filtered orders recorded between 1 January 2024 and 31 December 2024.

**SQL concepts applied:** `WHERE` and date-range filtering.

**Business relevance:** Date-based filtering allows the examination of activity within a defined reporting period.

### Product Performance Analysis

Compared products using recorded sales value, quantity sold, average unit price, and order frequency.

**Results:**

* **Highest recorded sales value:** Chair — 195,620.11.
* **Highest quantity sold:** Chair — 562 units.

**Key Insight:**

Chairs ranked highest in both recorded sales value and quantity sold. This indicates strong performance across these two measures in the dataset.

**Business relevance:** Product-level analysis can support inventory planning and help businesses evaluate which products contribute most to recorded sales.

### Payment Method Analysis

Counted records associated with each payment method.

**Key Finding:**

* **Most frequently recorded payment method:** Online — 258 records.

**Key Insight:**

Online was the most frequently recorded payment method in the dataset.

**Business relevance:** Understanding payment method distribution can help businesses assess payment usage and compare payment methods with order outcomes.

### Yearly Sales Analysis

Grouped the records by year to compare unique order counts, recorded sales values, and average record values.

**Results:**

| Year | Total_Orders  |  Total_Sales_Value   | Average_Record_Value |
| ---- | ------------: | -------------------: | -------------------: |
| 2023 |           510 |           552,643.24 |             1,083.61 |
| 2024 |           459 |           480,235.87 |             1,046.27 |
| 2025 |           231 |           231,882.85 |             1,003.82 |

*Values are rounded to two decimal places.*

**Key Insights:**

* 2023 recorded the highest number of unique orders, with 510.
* 2023 also had the highest recorded sales value, at 552,643.24.
* Recorded sales value decreased from 552,643.24 in 2023 to 480,235.87 in 2024.
* The average record value declined across the three years.

**Business relevance:** Comparing yearly order counts and sales values helps identify changes in recorded business activity over time.

The 2025 covers the first six months (January-June) of the year, so a full-year comparison cannot be made.

### Data Quality Assessment

Checked selected columns for NULL values:

* `OrderID`
* `Date`
* `Product`
* `Quantity`
* `TotalPrice`

**Result:** No NULL values were identified in the selected columns.

**Key Insight:**

The selected columns were complete with respect to NULL values in the records examined.

## Key Business Findings

The analysis produced the following findings:

1. **Order Status:** Cancelled was the most frequently recorded status, with 250 orders out of 1,200 (20.83%).

2. **Product Performance:** Chairs had the highest recorded sales value (195,620.11) and the highest quantity sold (562 units).

3. **Payment Methods:** Online was the most frequently recorded payment method, with 258 records.

4. **Yearly Performance:** 2023 recorded the highest number of unique orders (510) and the highest recorded sales value (552,643.24) among the three years analyzed, but 2025 covers only first 6 months of the year so a full year comparison cannot be carried out.

5. **Data Quality:** No NULL values were identified in the five selected columns checked for missing values.

## Business Recommendations

Based on the findings, the following actions are recommended:

1. **Order Management:** Review cancellation and return records to identify common reasons and opportunities to improve order completion and customer experience.

2. **Inventory Planning:** Use product sales and quantity data to inform inventory planning for high-performing products, including chairs.

3. **Payment Analysis:** Compare payment methods with order statuses to evaluate differences in order outcomes.

4. **Sales Performance Monitoring:** Track yearly order counts and sales values to monitor changes in business performance, ensuring that comparisons use consistent reporting periods.

## Project Files

* `README.md` — Project overview, methodology, findings, and recommendations.
* `Ecommerce_analysis.sql` — SQL queries used to conduct the analysis.
* `screenshots/` — Screenshots of selected SQL queries and results.
* `dataset/` — Source dataset used for  the analysis

## Conclusion

This project demonstrates the use of Microsoft SQL Server to analyse e-commerce order data through filtering, sorting, grouping, aggregation, date-based analysis, and data quality checks.

The analysis identified cancelled orders as the most frequent order status, chairs as the leading product by recorded sales value and quantity sold, online as the most frequently recorded payment method, and 2023 as the year with the highest recorded sales value.

The project strengthened practical SQL skills and demonstrated how query results can be translated into business findings and actionable recommendations.
