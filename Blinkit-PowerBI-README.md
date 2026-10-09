# Blinkit Grocery Sales Analysis | Power BI

A Power BI dashboard project analysing grocery sales performance across product categories and outlet characteristics. The report brings sales, item counts, customer ratings and outlet comparisons into one interactive view to support retail performance analysis.

## Dashboard preview
[grocery data 2.pdf](https://github.com/user-attachments/files/33246664/grocery.data.2.pdf)
> The dashboard preview is a static image. The interactive Power BI report is not publicly accessible through my university account.

## Project objective

Analyse the provided Blinkit grocery dataset to understand how sales are distributed across product categories, fat-content labels, outlet sizes, outlet location tiers, outlet types and establishment years.

## Tools used

- **Power BI** — dashboard design, KPI cards, charts, tables and interactive filters
- **CSV** — source dataset

## Dashboard KPIs

| KPI | Dashboard result |
| --- | ---: |
| Total sales | $1.20M |
| Average sales | $141 |
| Number of items (records) | 8,523 |
| Average rating | 4.0 / 5 |

*The dashboard's “No of Items” measure is a count of dataset records, not a count of unique products. The provided dataset does not identify individual customer transactions, so average sales refers to the average reported sales value per record. The dollar symbol follows the dashboard's display.*

## Dashboard features

- **Product performance:** Sales by item type and fat content
- **Outlet performance:** Sales by outlet size, location tier, establishment year and outlet type
- **Outlet comparison table:** Total sales, item count, average sales, average rating and item visibility
- **Interactive filters:** Outlet location type, outlet size and item type
- **Metric selector:** Switch between sales, average sales, item counts and ratings in the product analysis area

## Findings

1. **Supermarket Type1 leads combined sales**, with approximately **$787.55K**. This is a combined total across records in that outlet category, not a per-store comparison.
2. **Tier 3 has the highest combined sales** at **$472.13K**, followed by Tier 2 (**$393.15K**) and Tier 1 (**$336.40K**).
3. **Medium-sized outlets contribute the largest share of sales**, approximately **$507.90K** (42.3% of total sales), followed by Small (**$444.79K**) and High (**$248.99K**).
4. **Fruits and Vegetables and Snack Foods are the highest-selling product categories**, each generating approximately **$0.18M** in reported sales.
5. **Low Fat-labelled products account for more total sales** (**$776.32K**) than Regular-labelled products (**$425.36K**) in the dashboard.

These results describe the dataset. Differences in category size and outlet counts mean higher total sales do not necessarily indicate better performance per product or store.

## Business considerations

- Review the product categories contributing the most sales when planning category-level inventory and promotions.
- Compare performance per outlet before making decisions based on total sales by outlet type or location tier.
- Investigate why outlet sizes and locations contribute different shares of sales; further information would be needed to establish causes.



## How to explore

1. View the dashboard screenshot above or open the [grocery data 2.pdf](https://github.com/user-attachments/files/33246684/grocery.data.2.pdf)
2. Explore the [CSV dataset][BlinkIT Grocery Data.csv](https://github.com/user-attachments/files/33246690/BlinkIT.Grocery.Data.csv)

3. If a `.pbix` report file becomes available for sharing, it can be added to the repository to allow others to open the report in Power BI Desktop.

## Dataset note

This is an analysis of a **provided Blinkit-themed sample dataset**. It is not a claim of access to Blinkit's internal live sales records.
