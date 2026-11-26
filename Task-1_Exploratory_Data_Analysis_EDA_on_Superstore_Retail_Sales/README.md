# Datheon: Data Analytics & Power BI Internship
# Task 1: Exploratory Data Analysis (EDA) on Superstore Retail Sales

## Goal
Perform data wrangling, missing-value profiling, and uncover commercial sales distributions.

## Approach
- **Data wrangling:** the raw CSV contained three sheets stacked in one file (Orders, People, Returns). I separated them, kept 9,994 clean order rows, fixed data types and parsed the dates.
- **Data quality:** profiled missing values and duplicates, and explained the 806 blank rows.
- **Analysis:** customer purchase volume, monthly seasonality, category-wise revenue and discount sensitivity.
- **Validation:** the last notebook cell checks the final numbers and prints "All checks passed".

## Dataset Summary

| Metric | Value |
|--------|-------|
| Order rows | 9,994 |
| Customers | 793 |
| Period | Jan 2015 to Dec 2018 (48 months) |
| Total sales | about 2.30M |
| Total profit | about 286K (12.5% margin) |

## Key Findings

1. **Discounts above 20% lose money.** Margin is 29.5% with no discount and negative in every band above 20%.
2. **Tables and Bookcases drag Furniture down.** Furniture is about 32% of sales but only about 6% of profit.
3. **Top customers are not always profitable.** The #1 customer by sales has a negative profit, and 19.5% of customers lose money.
4. **Sales are seasonal.** September, November and December give about 43% of a typical year's sales.
5. **Sales grow faster than profit.** In 2018, sales grew 20.4% but profit only 14.2%.

Full evidence, recommendations and limitations: [Executive_Takeaways.md](Executive_Takeaways.md)

## Visual Highlights

<table>
  <tr>
    <td width="33%"><img src="Charts/01_profit_by_subcategory.png" alt="Profit by sub-category"><br><sub>Profit by sub-category</sub></td>
    <td width="33%"><img src="Charts/02_discount_vs_profit.png" alt="Discount vs profit"><br><sub>Discount vs profit</sub></td>
    <td width="33%"><img src="Charts/03_margin_by_discount_band.png" alt="Margin by discount band"><br><sub>Margin by discount band</sub></td>
  </tr>
  <tr>
    <td width="33%"><img src="Charts/03b_profit_by_discount_band.png" alt="Profit by discount band"><br><sub>Profit by discount band</sub></td>
    <td width="33%"><img src="Charts/04_top10_customers.png" alt="Top 10 customers"><br><sub>Top 10 customers</sub></td>
    <td width="33%"><img src="Charts/05_orders_per_customer.png" alt="Orders per customer"><br><sub>Orders per customer</sub></td>
  </tr>
  <tr>
    <td width="33%"><img src="Charts/06_monthly_sales.png" alt="Monthly sales"><br><sub>Monthly sales</sub></td>
    <td width="33%"><img src="Charts/07_seasonality_by_year.png" alt="Seasonality by year"><br><sub>Seasonality by year</sub></td>
    <td width="33%"><img src="Charts/08_avg_sales_by_calendar_month.png" alt="Average sales by month"><br><sub>Average sales by month</sub></td>
  </tr>
  <tr>
    <td colspan="3"><img src="Charts/09_sales_profit_by_group.png" alt="Sales and profit by category, region and segment"><br><sub>Sales and profit by category, region and segment</sub></td>
  </tr>
</table>

## How to Run

1. **Download the dataset:** open the [Data Set folder](Data%20Set), click `superstore_sales.csv`, then click the download button.
2. **Open the notebook in Google Colab:**
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RabiaMaqsood-01/Datheon_Data_Analytics_-_Power_BI_Internship/blob/main/Task-1_Exploratory_Data_Analysis_EDA_on_Superstore_Retail_Sales/Task_1_Exploratory_Data_Analysis_EDA_on_Superstore_Retail_Sales.ipynb)
3. **Upload the dataset:** click the folder icon on the left side of Colab, then the upload icon, and choose `superstore_sales.csv`.
4. Click **Runtime → Run all**.
5. The last cell prints "All checks passed" when everything has run correctly.

To run locally: `pip install -r ../requirements.txt`, put `superstore_sales.csv` next to the notebook, and open the notebook in Jupyter.

## Folder Contents

| Item | Description |
|------|-------------|
| Notebook (`.ipynb`) | Full analysis with code, charts and notes |
| `Executive_Takeaways.md` | 5 executive takeaways plus a bonus one, with limitations |
| `Charts/` | PNG charts exported from the notebook |
| `Data Set/` | Original `superstore_sales.csv` |
