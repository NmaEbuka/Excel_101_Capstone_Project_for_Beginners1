# Excel_101_Capstone_Project_for_Beginners1
Monthly Sales Tracker for a Small Retail Business
## 1. Project Brief
This project is to test basic skills in Excel. It is beginner-friendly. It is also business-focused and can be used as a portfolio item for data analyst beginners.
### Business Problem:
Client: Zara's Boutique (A small clothing retail business).

Situation: Zara currently tracks her daily sales on paper. She wants a clean, professional Excel workbook that shows her monthly sales performance, calculates her totals and averages, and is easy to update every day.

Deliverables: a. A ceaned data presented on a table. b. Monthly summary of sales. c. Line chart and bar chart showing daily revenue over 30 days and total revenue by product category respectively.

## Process Note
### Data Source
Since the business is fictional the data used is also fictional. Excel formulas and functions were used to generate the data in the table.
The table has the following columns:
|Column|Data Type|Formula or Function|
|----------|-----------|----------|
Date| Data Type | Type in the 1st day of January 2025 and drag for the full month|
Day | Text | January 1st 2025 is on a Wednesday. Type and drag down to generate for the full month|
Product Category | Text | Use 3 categories: Clothing, Accessories, Footwears |
Units Sold | Number | Enter: =RANDBETWEEN(1,50 to generate random numbers between 1 and 50 |
Unit Price | Currency| Clothing: 8500, Accessories: 3200, Footwear: 12,000|
Total Revenue | Currency | Formula (Unit sold * unit price) |
Above Revenue? | Text| Formula: =IF(F17>50000,"Yes","No")

### Methodology
#### Data Preparation
|Issue Found | Action Taken | Tools/Methods | Reasons
|----------|----------|----------|-----------|
|Unit price keeps changing because of the use of the RANDBETWEEN function| Copied and pasted the whole table as values in a new sheet. This became my working data | Copy & Paste (as value) | Total Revenue also kept changing because it was a derived value from unit sold|
| After pasting the value from the previous step, dates change to the 'General' format | Changed the format of the date to the 'Short Date' format | The Number Tab in the Home ribbon | Dates cannot be worked with in the 'General' format for analysis |
|The numbers in the Unit Price and Total revenue columns were in the General format | Changed the format to Currency and then the sign to the Nigerian Naira |The Number Tab in the Home ribbon | The analysis is a financial report of a Nigerian business. It makes sense for the price and revenue to be the Nigerian currency|

This new sheet is called the "Working Data"

#### Data Analysis
On a new sheet called "Monthly Summary"
Monthly KPIs:

Total Revenue: SUM(Table1[Total Revenue]) 

NB: Table 1 is the table containing the working data on the working data sheet.

Total Revenue is the column.

Average Daily Revenue: AVERAGE(Table1[Total Revenue])

Highest Revenue: MAX(Table1[Total Revenue])

Lowest Revenue: MIN(Table1[Total Revenue])

Total days above revenue: COUNTIF(Table1[Above Average?], "Yes")

Revenue (Clothing): =SUMIF(Table1[Product Category], "Clothing", Table1[Total Revenue])

Revenue (Accessories): =SUMIF(Table1[Product Category], "Accessories", Table1[Total Revenue])

Revenue (Footwear): SUMIF(Table1[Product Category], "Footwears", Table1[Total Revenue])
#### Alternative Formula if the formula is typed instead of directly selecting the colomn from the table
Total Revenue: SUM(F2:F32) 

Average Daily Revenue: AVERAGE(F2:F32)

Highest Revenue: MAX(F2:F32)

Lowest Revenue: MIN(F2:F32)

Total days above revenue: COUNTIF(G2:G32, "Yes")

Revenue (Clothing): SUMIF(C2:C32, "Clothing", F2:F32)

Revenue (Accessories): SUMIF(C2:C32, "Accessories", F2:F32)

Revenue (Footwear): SUMIF(C2:C32, "Footwears", F2:F32)

NB: This second set of formula work if the analysis is done on the same sheet as the working data.
NB2: To check that the revenue for each product category is correct, calculate the sum of all three category. If it equals the total revenue, it is correct. Otherwise, recheck.

### Limitations
