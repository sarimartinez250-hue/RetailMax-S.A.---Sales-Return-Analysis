# 📈💰📊 RetailMax S.A. - Sales & Returns Analysis
An interactive Power BI project focused on sales performance, profitability, sales targets, and product returns. This project demonstrates the application of data cleaning, data transformation,
data modeling, DAX calculations, and data visualization to turn raw data into meaningful business insights.

## 🗂️👨🏻‍💻 Project Overview
RetailMax S.A. is a fictional retail company used to develop and end-to-end Business Intelligence project with Power BI.
The goal of this project is to explore sales and returns data, evaluate business performance, identify trends and anomalies, and support data-driven decision-making through and interactive
dashboard.
Rather than focusing only on visual design, this project emphasizes analytical thinking: understanding the data, defining meaningful metrics, identify patterns, and asking further questions based
on the results.

Dataset: fictional/syntethic data
Tools: Microsoft Power BI, Power Query, DAX, Microsoft Excel
Project type: Business Intelligence and Data Analytics

## 🎯 Business Objectives
The report was designed to answer questions such as:
- How are sales and profitability performing over time?
- Which regions, salespeople, product categories, and sales channels contribute most to sales?
- How do actual sales compare with sales targets?
- How do discounts related to net sales?
- Which categories and products generate the highest refund amount?
- What are the most common reason for product returns?
- How do returned units relate to their financial impact?
- Are the unusual trends or periods that require further investigation?

## ⚙️💻 Tools and Technologies
- Power BI Desktop: Report development, data modeling, DAX measures, interactive visuals, and navigation.
- Power Query: Data extraction, transformation, cleaning, merging, and preparation.
- DAX(Data Analysis Expressions): Business metrics, financial calculations, time-based analysis, and key performance indicators.
- Microsoft Excel: Source data preparation and inspection.

## ⭐⭐⭐⭐⭐ Data preparation and Quality
This project involved preparing and integrating multiple datasets into a structure suitable for analysis.

Key data tasks preparation included:
- Combining monthly sales files into consolidated yearly datasets and integrating them into a central sales fact table.
- Identifying missing and invalid value in important fields.
- Creating a cleaned quantity field to adress missing quantities, using sales amounts and unit prices where was appropiate.
- Identifying invalid Product IDs and recovering product identifiers when a reliable matching unit cost was available.
- Handling missing customer identifiers using an explicit unknown-customer classification when the original customer could not be reliably identified.
- Enriching sales records with region information using salesperson assignments.
- Preparing a calendar table and a YearMonth period field to support time-based analysis.
- Integrating return-related information with customer, product, region, and date attributes.
- Applying a return eligibility rule based on the number of days between shipping and the return date.

These transformations were intended to improve data consistency, support reliable calculations, and make the resulting model more useful for business analysis.

## 📐 Data model
The project uses a dimensional modeling approach to organize the data and support filtering across report pages.

The model includes:
- FactSales: Central sales transaction data.
- Returns: Return requests, returned quantities, return reasons, eligibility, and refund amounts.
- Calendar: Date attributes used for time-based analysis such as Year, Month, WeekDay, etc.
- Products: Product attributes, including category, product name, and list price.
- Customers: Customer information, including city.
- Salespeople: Salesperson attributes and regional assignments.
- Region: Regional classification.
- Monthly_Targets: Monthly sales targets by region and reporting period.
- Period: Year, Month, MonthName, and YearMonth attributes.

Relationships and filter propagation were designed to allow users to analyze business performance across relevant dimensions. 
Power Query merges were also used to enrich return records with attributes needed for regional and customer-level analysis.

## 📑 Dashboard pages
The report contains four pages, each one designed for a specific purpose.
1. Main. The landing page introduces the RetailMax S.A. report and provides navigation to the main analytical sections.

2. Exectuive Overview. Provides a high.level view of overall business performance through KPI cards and trend visualizations.
   
   The page focuses on key financial indicators, sales trends, year-over-year performance, and product-level contributions to sales and gross profit.

4. Sales Performance. Explores sales performance across business dimensions, including region, salesperson, prodcut category, and sales channel.

5. Return Analysis. Examines products returns from operational and financial perspectives.
   
   The report includes indicators such as return requests, approved and rejected returns, approval rate, returned units, refund amount, order return rate, and unit return rate.

   Its visualizations explore refund trends over time, the distribution of return reasons over months, refund amounts by category and product, approved returns by region, and the relationship
   between returned units and refund amounts.

## 👁️📌 Selected Analytical Observations
The dashboard supports several useful analytica investigations.
- Refund trends and anomalies. Monthly refund amounts can be compared to identify unusually high or low periods.
  For example, the report highlights a substantial difference between November and December 2025, providing an opportunity to investigate which categories, products, or return reason contributed
  to the change.

- Return reasons. A 100% stacked column chart shows the relative distribution of return reasons by month. This makes it possible to comparethe composition of return acros periods, including when
  the total number of returned units differs.

- Product-level refund analysis. A Category → Product hierarchy allows users to begin with a high-level category comparison and drill down into individual products. This supports more
  detailed investigation of categories or products associated with high refund amounts.

- Returned units versus refund amount. The combined line and column chart compares returned quantities with their financial impact.
  For example, July 2024 recorder 64 returned units and a refund amount of $52,212.74, while December 2025 recorded 59 returned units and $51,751.58 in refunds.
  This comparison illustrates why return volume alone does not fully explain financial impact. Differences in product prices, product mix, and other factors may help explain the variation and
  can be investiated using the report filters.

- Regional analysis. Regional comparisons help identify where approved returns are concentrated. However, a high number of returns does not necessarily indicate a high return rate. Return
  counts should be interpreted alongside order volumen and other relevant measures.

These observations illustrate how the dashboard can be used not only to summarize performance but also to generate questions for further analysis.

## 🔐 Key measures
The project included measures designed to evaluate sales performance and return behavior.

### Sales Analysis
- Gross Sales
- Net Sales
- Gross Profit
- Gross Margin
- Average Order Value (AOV)
- Total Orders
- Average Shipping Days
- Discount Amount and Discount Percentage
- Sales Target Attainment
- Year-to-date and prior-period comparisons
- Year-over-year growth and rolling-period analysis

### Return Analysis
- Returns requests
- Returns Approved
- Returns Rejected
- Returns Approval Rate
- Returned Units
- Orders Return Rate
- Units Return Rate
- Average Refund per Returned Unit

The measures support comparisons across time, regions, categories, products, and other available dimensions.

## 🗂️ Repository Structure
The repository is organized to make the report, supporting data, and documentation easy to explore.

### How to use the project
1. Clone or download this repository.
2. Open RetailMaxAnalysis.pbix using Power BI Desktop.
3. If Power BI request access to the source files, update the data-source paths to match their locations on your computer.
4. Refresh the data if source files are available and the queries are configured correcly.
5. Explore the report using the slicers, navigation buttons, and drill-down functionality.

## 🚧 Assumptions and Limitations
- RetailMax S.A. is fictional, and the dataset is synthetic or modified for educational and portfolio purposes.
- Missing or invalid source values may require explicit assumptions during data preparation.
- Product identifier recovery is performed only where a reliable matching value is available.
- Customer records that cannot be reliably identified are classified as unknown.
- Return eligibility is determined using a 90-day threshold from shipping date. Refund amounts are set to zero returns outside that eligibility window under the project's business rules.
- Observed trends and anomalies indicate areas for further investigation; they do not necessarily establish causation.

These assumptions should be considered when interpreting the results.

## 💡🧠 Skills demonstrated
- Data cleaning and transformation with Power Query
- Data modeling and relationship design
- DAX measures and business calculations
- Time-based analysis
- KPI development
- Interactive dashboard design
- Drill-down analysis and filter interactions
- Data quality assessment and explicit handling of assumptions
- Business-oriented data storytelling

## 📍 Project Outcome
RetailMax S.A. represents a practical application of Business Intelligence principles, from preparing imperfect data to developing an interactive report that supports meaningful analysis.

The main objective was not simply to create visually, appealing charts, but to build a report that helps users understand business performance, investigate unusual patterns, and ask better
questions of the data.

## 👩🏻‍💻 Author
Jessica Sarai Martinez Galicia

## 🛠️ Tools
Power BI • Power Query • DAX • Excel

## 📋 Project
Sales & Returns Analysis
