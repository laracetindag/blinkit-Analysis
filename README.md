# blinkit-Analysis
Business problem
The project investigates how product characteristics and outlet attributes relate to the sales performance of the Blinkit grocery dataset. The analysis addresses four headline measures: total sales, average sales, item count and average rating. It also compares results by item category, fat content, outlet type, size, location tier and establishment year.
Tools
- SQL (T-SQL): Data cleaning, aggregation, grouping and sales-percentage calculations.
- Power BI: Interactive dashboard, visuals, KPI cards and slicers.
- CSV and JSON: Provided source data files.
Dataset and KPI overview
The supplied dataset contains 8,523 rows, covering 10 outlet identifiers and 1,559 distinct item identifiers. The measures below are calculated directly from the included CSV; the original project dashboard rounds its KPI cards for display.
Metric	Result
Total sales	$1,201,681.48
Average sales per data row	$140.99
Records / item entries	8,523
Unique item identifiers	1,559
Average rating	3.97 / 5 (shown as 4.0)


Metric note: The supplied SQL reference calculates Number of Items using COUNT(*), which is 8,523 records, rather than 1,559 distinct product identifiers. The source data does not provide transaction IDs, so average sales is calculated per row, not verified per customer transaction. Currency symbols follow the project dashboard's presentation; the CSV does not specify a currency.
Findings
1. Tier 3 outlets lead sales: $472,133.03, ahead of Tier 2 ($393,150.64) and Tier 1 ($336,397.81). These are combined sales amounts, not average sales per outlet.
2. Medium-sized outlets account for the largest sales share: $507,895.73, or approximately 42.27% of total sales. Small outlets contribute about 37.01% and high-size outlets about 20.72%.
3. Fruits and Vegetables and Snack Foods are the leading product categories: approximately $178,124.08 and $175,433.92 in sales, respectively.
4. Low Fat-labelled items account for more reported sales: $776,319.68 versus $425,361.80 for Regular-labelled items, after standardising inconsistent values.
5. Supermarket Type1 has the largest combined sales: $787,549.89. Outlet counts and mix should be considered before drawing conclusions about store-level performance.
These are descriptive observations, not proof that outlet size, location or fat content caused higher sales.
Data cleaning and analysis
The source CSV contains inconsistent values in the Item Fat Content column. The cleaning step standardises:
- LF and low fat → Low Fat
- reg → Regular
The supplied data also has 1,463 missing values in Item Weight. Those blanks are preserved in the raw files. The SQL script includes KPI and grouping queries for product type, outlet location, outlet size, outlet type and establishment year. See [`sql/blinkit_analysis.sql`](sql/blinkit_analysis.sql).
Power BI dashboard
The report uses KPI cards for total sales, average sales, item count and rating, alongside visuals for:
- Sales by product type and fat content
- Sales by outlet location, outlet size and outlet establishment year
- Outlet type comparisons and filter controls
The filters help compare subsets of the dataset without changing the source records.
Repository structure
Blinkit-Sales-Analysis/
├── README.md
├── data/
│   ├── blinkit_grocery_data.csv
│   └── blinkit.json
├── sql/
│   └── blinkit_analysis.sql
├── docs/
│   ├── project_requirements.pdf
│   └── sql_query_reference.docx
└── images/
    ├── README.md
    └── dashboard.png   
How to explore
1. Review the source data in [`data/blinkit_grocery_data.csv`](data/blinkit_grocery_data.csv).
2. Import the CSV into SQL Server, naming the table blinkit_data and mapping the column names to underscore-separated names used in the provided SQL script.
3. Review or run [`sql/blinkit_analysis.sql`](sql/blinkit_analysis.sql) to clean the fat-content labels and reproduce the KPIs.
4. Use the CSV in Power BI Desktop if you want to recreate or extend the dashboard. The original .pbix report is not included in these source files.
Source materials
This is a portfolio project based on a provided Blinkit sample dataset and accompanying analysis requirements and SQL reference. The repository includes the source brief and SQL document for transparency. It is not a claim of access to Blinkit's internal company records.
