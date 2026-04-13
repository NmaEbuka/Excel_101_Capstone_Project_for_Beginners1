<img width="715" height="30" alt="image" src="https://github.com/user-attachments/assets/6699afc0-fbc7-46b7-a563-223a09c51c35" /><img width="700" height="30" alt="image" src="https://github.com/user-attachments/assets/303aa53b-2b89-462f-96a0-ffff9623d71e" /># Excel_101_Capstone_Project_for_Beginners1
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
#### Data Analysis
Monthly KPIs:
Total Revenue()
Average Daily Revenue ()
Highest Revenue ()
Lowest Revenue ()
Total days above revenue ()
Revenue (Clothing)
Revenue (Accessories)
Revenue (Footwear)
### Limitations
### Time log
