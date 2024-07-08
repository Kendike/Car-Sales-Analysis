# Car-Sales-Analysis
## Overview 
The car sales Data Analysis project aims to provide comprehensive insights into vehicle sales trends and patterns reveal Top Selling Models and conduct Profitability Analysis. This project involves the collection, cleaning, analysis and visualization of car sales data to help stakeholders make infomred decisions. This project show cases data analytics techniques and tools to derive meaniful conclusions from raw data.
### Tools
- SQL- Data Collection, Data Cleaning
- Tableau - Data Analysis, Visualization.
### Data Cleaning and Preparation
1. After careful study of the data set on big query a new table was created to remove irrelavant columns with the below query
``Create Table project-012022-363821.Project.New_Cars_Data_Set as
SELECT `Purchase Date` , Vehicle, `P PRICE`, `TOTAL COST`,`SALE PRICE`,PROFIT, `%`, `SALE DATE`,
 FROM `project-012022-363821.Project.New_Car_Data`` 
2. Following the creation of the new table, field names were standardized for clarity and duplicates were removed with following query.
``SELECT Purchase_Date,Purchase_Price,
Vehicle,Total_Cost,Sale_Price,Profit,
Percentage_Profit,Sale_Date
FROM(
SELECT DISTINCT
`Purchase Date` as Purchase_Date,
Vehicle,
`P PRICE` as Purchase_Price,
`TOTAL COST` as Total_Cost,
`SALE PRICE` as Sale_Price,
PROFIT as Profit,
`%` as Percentage_Profit,
`SALE DATE` as Sale_Date
 FROM `project-012022-363821.Project.New_Cars_Data_Set`)``

3. Empty or null cells within the dataset were identified and removed to ensure data completeness and accuracy.
``WHERE
Purchase_Date IS NOT NULL AND Vehicle IS NOT NULL AND Purchase_Price IS NOT NULL
AND Total_Cost IS NOT NULL AND Sale_Price IS NOT NULL AND Profit IS NOT NULL AND
Percentage_Profit IS NOT NULL AND Sale_Date IS NOT NULL``
The columns where in the right format the data was exported to tableau for analysis and visualization.
### Data Analysis
- 1 Calculation of Key KPIs
Key performance indicators (KPIs) such as Average Car Sales, Average Profit, Total Sales, Total Profit, and Total Number of Cars Sold were calculated using Tableau's calculated fields feature.
- 2 Sorting and Analysis in Tableau
Using Tableau, the dataset was sorted and analyzed to identify:
  - Best Selling Cars: Identified the top-selling car models based on sales volume.
  - Most Profitable Vehicles: Determined the models yielding the highest average profit per unit sold.
  - Best Performing Month: Analyzed sales performance across months to identify the peak sales month.
- 3 Bar Chats were used to Visualize most profitable vehicles and top selling vehicles and area chart for best selling month.
### Data Visualization
<img width="560" alt="Car_Sales" src="https://github.com/Kendike/Car-Sales-Analysis/assets/123019944/0d90df5c-c768-4fef-9fcb-6561ca4cfe98">

### Conclusion
Based on the comprehensive analysis of car sales data, several key insights have been uncovered:
- Top Selling Cars: The Hyundai Tucson, Nissan Pathfinder, and Ford have emerged as the top-selling models in our dataset. The Hyundai Tucson leads in sales volume, followed closely by the Nissan Pathfinder and Ford.
- Most Profitable Models: In terms of profitability, the Hyundai, Land Rover, Nissan Pathfinder and Ford models stand out, generating the highest average profits per unit sold. These models have demonstrated strong market demand and pricing power, contributing significantly to overall profitability.
- Best Performing Month: September 2023 was identified as the best-selling month, indicating a seasonal peak in consumer demand. This insight suggests potential opportunities for targeted marketing campaigns or inventory management strategies during peak months to maximize sales and profitability.

- Key Performance Indicators (KPIs)
  - Average Profit: The average profit per car sold was $600.
  - Number of Cars Sold: A total of 2849 cars were sold during the analyzed period.
  - Total Profit: The total profit generated from car sales amounted to $1,758,133.79
  - Total Sales: The total sales revenue generated from car sales amounted to $11,968,694.69.
### Recommendation
Recommendations
Based on the findings, the following recommendations are proposed to capitalize on strengths and address areas of improvement:
- Focus on Top Selling Models: Allocate additional resources and marketing efforts towards promoting the Hyundai Tucson, Nissan Pathfinder, and Ford models. Enhance dealership incentives and promotional campaigns to maintain or increase their market share.
- Profitability Strategies: Continue to prioritize the Hyundai, Land Rover, Nissan Pathfinder and Ford models due to their high profitability. Explore opportunities to introduce higher-margin vehicle variants or upsell accessories to further boost profitability per unit.
- Seasonal Strategies: Given the peak in sales observed in September 2023, develop seasonal sales strategies to capitalize on similar trends in future years. Adjust inventory levels and promotional activities to align with seasonal fluctuations in consumer demand.
