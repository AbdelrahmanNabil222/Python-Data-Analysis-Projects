# Adidas US Sales Analysis (Python)

Exploratory data analysis of Adidas US sales using Python: data cleaning, feature engineering, and static and interactive visualizations to understand sales and profit across regions, products, sales methods, and time.

## Business Questions
- Which regions generate the most sales?
- Which products contribute the most to operating profit?
- Which days of the week are the most profitable?
- How do sales and profit change over time and by sales method (In-store, Online, Outlet)?

## Dataset
- **Source:** Adidas US Sales dataset (add the link here)
- **Size:** 9,648 rows and 12 columns (9,641 rows after cleaning)
- **Period:** January 2020 to December 2021
- **Columns:** Retailer, Retailer ID, Invoice Date, Region, State, City, Product, Price per Unit, Units Sold, Total Sales, Operating Profit, Sales Method

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly Express, Jupyter Notebook

## Workflow

### 1. Data Cleaning
- Checked for duplicate rows (none found).
- Found missing values: 7 in `Region` and 2 in `Price per Unit`.
- Filled the missing prices using the average price of the same state and region.
- Removed the 7 rows with a missing region (9,641 rows remained).
- Converted `Invoice Date` from Excel serial numbers to real dates.

### 2. Feature Engineering
- Created a `Day` column (day of the week) to analyze profit by weekday.
- Calculated each product's share of total operating profit.

### 3. Analysis
- Total sales by region
- Profit share by product
- Average operating profit by day of the week

### 4. Visualization
- **Matplotlib and Seaborn:** profit and sales over time, sales trend by sales method, number of transactions by sales method, average sales by method, and a joint plot of sales over time.
- **Plotly (interactive):** profit by product and sales method, sales share by method (pie chart), and sales by state and region (sunburst).

## Key Insights
1. **The West region leads in sales** with about $26.9M, roughly 30% of the total, followed by the Northeast ($18.6M) and the Southeast ($16.3M). The South ($14.4M) and the Midwest ($13.6M) are the lowest.
2. **Men's Street Footwear is the top profit driver** with about 25% of total operating profit, followed by Women's Apparel (20.7%) and Men's Athletic Footwear (15.6%).
3. **Profit is well diversified:** no product category exceeds a quarter of total profit, and the six main products each contribute between 11.7% and 25%.
4. **Thursday and Friday are the most profitable days:** the average profit per transaction is about $4,000 on Thursday and $3,800 on Friday, compared with about $3,000 on Saturday, the lowest day.

## Recommendations
- Keep investing in the **West region**, and study what drives the weaker results in the Midwest and South.
- Prioritize inventory and promotions for **Men's Street Footwear** and **Women's Apparel**.
- Schedule campaigns and stock replenishment around **Thursday and Friday**, when profit per transaction is highest.
