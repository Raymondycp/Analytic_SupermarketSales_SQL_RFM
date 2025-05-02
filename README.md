# Supermarket Sales RFM Analysis

## Overview

This project performs an **RFM (Recency, Frequency, Monetary)** analysis on a supermarket sales dataset to segment customers based on their purchasing behavior. The analysis uses SQL (via DuckDB) and Python for data processing, visualization, and customer segmentation. The goal is to identify key customer segments to inform marketing strategies and improve customer retention and profitability.

## Objectives

- **Analyze Sales Data**: Understand the profitability of different product categories.  
- **Customer Segmentation**: Use RFM analysis to categorize customers into segments.  
- **Visualizations**: Create insightful charts and dashboards to communicate findings effectively.  
- **Business Insights**: Provide actionable recommendations based on customer behavior and sales trends.

## Dataset

The dataset (`Supermart.csv`) contains 9,994 records of supermarket sales with the following columns:

- `order_id`: Unique identifier for each order.  
- `customer_name`: Name of the customer.  
- `category`: Product category   
- `subcategory`: Subcategory of the product.  
- `city`: City where the order was placed.  
- `order_date`: Date of the order (converted to `datetime64`).  
- `region`: Region of the order.  
- `sales_amount`: Total sales amount for the order.  
- `discount_amount`: Discount applied to the order.  
- `profit_amount`: Profit from the order.  
- `state`: State where the order was placed.

Details:

- The dataset spans orders up to December 30, 2018\.  
- There are 50 unique customers.  
- The dataset is complete with no missing values.

## Key Steps

1. **Data Loading and Preprocessing**:  
     
   - The dataset is loaded using `pandas` and columns are renamed for consistency (e.g., `Order ID` to `order_id`).  
   - The `order_date` column is converted to `datetime64` format for time-based analysis.

   

2. **Business Questions**: The notebook addresses 10 business questions.  
     
3. **RFM Analysis**:  
     
   - **Recency**: Days since the customer's last purchase (relative to the max `order_date`: 2018-12-30).  
   - **Frequency**: Number of orders per customer.  
   - **Monetary**: Total sales amount per customer.  
   - **Segmentation**: Customers are grouped into segments (e.g., High-Value, High-Retention, Churn-Risk) based on RFM scores.  
   - **Visualizations**:  
     - **3D Scatter Plot**: Displays Recency, Frequency, and Monetary values for each customer.  
     - **Bar Plot**: Shows average RFM values by customer segment.  
     - **Pie Chart**: Illustrates the distribution of customers across segments.  
     - **Scatter Plot**: Plots Recency vs. Monetary to highlight customer behavior.

---

