# Superstore-Analysis-PowerBI

## Objective
In today's business landscape, data-driven decision-making is essential for success. The Superstore Sales Analysis and Forecasting project utilizes advanced analytics and visualization techniques to uncover patterns, trends, and key insights within a sales dataset. By leveraging Power BI, this project enables stakeholders to analyze historical sales performance and predict future trends using the Power BI Forecast tool. Through detailed sales analysis, it provides valuable insights that support strategic planning and decision-making, ultimately driving business growth and efficiency.

## Description
This repository includes all the essential files and resources for a thorough analysis of superstore sales data. Utilizing Power BI, a robust business intelligence tool, the project visualizes and examines various aspects of sales, such as customer behavior, product performance, and regional trends. The insights gained from this analysis help drive business optimization and strategic decision-making.

## Project Workflow

### Data Preparation
- Performed data cleaning tasks to ensure data quality, including:
  - Removal of null values
  - Elimination of unnecessary columns
  - Handling of duplicate records
  - Adjusting data types

### Data Modeling
- Created calculated measures and tables using DAX (Data Analysis Expressions) in Power BI
- Enhanced the dataset’s analytical capabilities for deeper insights
## DAX Code for Data Analysis
```DAX
#Created time-series table of sales for forecasting

TimeSeriesTable = 
SUMMARIZE(
  SuperStore_Sales_Dataset,
  SuperStore_Sales_Dataset[Order Date],
  "Total Sales", SUM(SuperStore_Sales_Dataset[Sales])
)  

#Calculate a measure to determine the number of days it took for delivery.
  DaysToDeliver = 
  DATEDIFF(
    SuperStore_Sales_Dataset[Order Date],
    SuperStore_Sales_Dataset[Ship Date],
    DAY
  )
```
### Data Analysis
- Conducted in-depth analysis using Power BI visualization techniques:
  - Identified sales trends
  - Analyzed region-wise sales
  - Explored category-wise sales
  - Extracted other key insights using matrices and charts

### Dashboard Creation
- Developed an interactive and dynamic dashboard in Power BI
- Integrated bookmark features for seamless navigation between different charts and visualizations
- Provided a comprehensive view of the data for better decision-making

### Sales Forecasting
- Leveraged Power BI's advanced forecasting feature to generate a 10-day sales forecast
- Assisted stakeholders in anticipating future trends and making informed decisions

## Dashboard Overview
The dashboard section provides a variety of interactive visualizations, enabling users to analyze and interpret historical sales data effectively. Key features include:

- **Tracking** monthly and yearly sales trends.  
- **Comparing** sales performance across various categories and sub-categories.  
- **Visualizing** the geographical distribution of sales.  
- **Identifying** top payment methods, customer segments, shipping modes, and other crucial insights.  

## Key Insights
The dashboard and forecasting page reveal several critical insights:

- **Sales Peaks:** Significant sales surges occur in February, August, and October, indicating recurring trends.  
- **Consistent Growth:** Sales in 2020 outperformed 2019, but the overall trend patterns remained steady.  
- **Top Sales Regions:** California leads in sales, followed closely by New York.  
- **Regional Contribution:** The West region accounts for the highest share of total sales.  
- **Preferred Payment Method:** Cash on Delivery (COD) emerges as the most popular payment option.  
- **Leading Customer Segment:** The consumer segment generates the highest sales volume.  
- **Top-Selling Category:** Office Supplies dominate as the highest-selling product category.  
- **Preferred Shipping Mode:** Standard Class is the most commonly chosen shipping method.  
- **Best-Selling Sub-Categories:** Phones and chairs rank as the top-selling sub-categories.

