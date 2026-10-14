# RetailMax Power BI Practice Project

Goal: practice a complete Power BI workflow: ETL in Power Query, data modeling, DAX measures, time intelligence, KPIs and dashboards.

## Folder structure
- Raw_Data/Sales_YYYY_MM.csv -> 48 monthly transaction files
- Raw_Data/Customers.csv
- Raw_Data/Products.csv
- Raw_Data/Salespeople.csv
- Raw_Data/Returns.csv
- Raw_Data/Monthly_Targets.csv

## ETL challenges intentionally included
1. Combine all monthly Sales files from a folder.
2. Normalize column names (one file uses Sales_Amount).
3. Convert inconsistent data types (Discount, Quantity, dates).
4. Handle missing CustomerID and Quantity values.
5. Detect an invalid ProductID (P9999).
6. Create/validate keys and relationships.
7. Standardize date fields.
8. Remove or flag bad records rather than silently ignoring them.

## Recommended model
Star schema:
DimDate -> FactSales
DimCustomer -> FactSales
DimProduct -> FactSales
DimSalesperson -> FactSales
FactReturns -> dimensions as appropriate
Targets can be modeled by Year/Month/Region.

## DAX challenges
Start with:
- Total Sales
- Total Cost
- Gross Profit
- Gross Margin %
- Units Sold
- Orders
- Average Order Value

Then:
- Sales YTD
- Sales MTD
- Previous Year Sales
- YoY Growth %
- YoY Growth Amount
- Rolling 3/6/12 month sales
- Sales vs Target
- Target Achievement %
- Return Rate
- Net Sales
- Sales by Customer/Category/Channel
- Top 10 Products
- Customer Rank
- Contribution %
- Running Total

## Suggested progression
Level 1: Clean and combine Sales files.
Level 2: Build the star schema.
Level 3: Create core DAX measures.
Level 4: Add Calendar + time intelligence.
Level 5: Add Returns and Targets.
Level 6: Build an executive dashboard.
Level 7: Build a sales-performance dashboard and drill-through pages.

Do not look at the solution first. Treat the dataset as a real company's imperfect data.
