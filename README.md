# AdventureWorks Sales Performance Dashboard 2024

<img width="1306" height="735" alt="Screenshot 2026-08-02 071230" src="https://github.com/user-attachments/assets/76e145db-5573-4e11-8594-f33128326dfb" />

## 🧰 Project Background
AdventureWorks is a fictional global company selling outdoor and cycling products across multiple regions, including Southeast Asia, Oceania, North America, and Europe. As the business scales, management needs a centralized, visual way to monitor sales performance, profitability, and product trends across different markets and time periods. This project builds an interactive Power BI dashboard to consolidate sales, profit, and order data from AdventureWorks' 2023-2024 transactions into a single, easy-to-read view.

## 🔐 Problem Statement
Without a consolidated reporting tool, stakeholders previously had to manually pull and cross-reference data from multiple sources (customer, product, territory, and sales tables) to answer basic business questions such as:
- Which products generate the highest sales and profit?
- Which countries and regions contribute the most revenue?
- How does sales performance trend month over month?
- Which product categories are most profitable?

This manual process is time-consuming, error-prone, and does not support quick, data-driven decision-making.

## 📊 Analysis

### Data Understanding
The dashboard is built from six datasets:
- **Dim Calendar** — date dimension for time-based analysis
- **Dim Customers** — customer demographic and profile data
- **Dim Products** — product catalog with category and pricing details
- **Dim Territories** — region and country mapping
- **Fact Table Sales** — transactional sales data (order date, quantity, sales, profit)
- **Fact Returns** — product return records

These tables are structured in a star schema, connecting fact tables to dimension tables for efficient filtering and aggregation.

### Data Preprocessing
- Verified and cleaned data types (dates, numeric fields) across all tables
- Established relationships between fact and dimension tables based on primary/foreign keys (ProductID, CustomerID, TerritoryID, Date)
- Created calculated measures for Total Sales, Total Profit, and Sum of Order Quantity
- Applied consistent formatting (currency and number units) for readability

### Analysis and Insight
- **Total Sales** reached 1.42M with **Total Profit** of 595.02K across roughly 1,000 units sold in 2024
- **Top-performing products** by sales include WindCutter S, Velocity Pro, and HydroFlask 750ml, each contributing over 100K in sales
- **Sales by country** shows a fairly even distribution, with United States (19.79%) and Germany (18.4%) as the top contributors, indicating a diversified international customer base rather than dependence on a single market
- **Monthly sales trend** shows notable volatility, with peaks around 102K-124K in certain months (e.g., early 2023 and early 2024) and dips below 20K in others, suggesting seasonal or promotional effects
- **Profit by category** shows Bikes as the dominant category (0.35M profit), significantly outperforming Accessories (0.13M) and Clothing (0.12M)

## 💡 Conclusion
- AdventureWorks' sales are broadly diversified across geography and product lines, reducing dependency risk on any single market
- Bikes are the primary profit driver, far ahead of Accessories and Clothing
- Sales performance fluctuates significantly month to month, pointing to seasonality or the impact of specific campaigns/promotions rather than steady, linear growth

## 🎯 Recommendations
1. **Double down on Bikes** — since this category drives the majority of profit, consider expanding the product line or increasing marketing investment here
2. **Investigate sales spikes and dips** — analyze what drove the high-performing months (e.g., promotions, seasonality) and replicate those conditions in lower-performing months
3. **Grow underperforming categories** — Accessories and Clothing have lower profit but could be cross-sold alongside Bikes to increase basket size
4. **Monitor regional performance closely** — while sales are diversified, tracking country-level trends over time can help identify emerging or declining markets early
5. **Extend the dashboard** with year-over-year comparison and customer segmentation to support deeper strategic decisions going forward

---

*Built with Power BI. Data used is illustrative/sample data based on the AdventureWorks dataset for learning purposes.*
