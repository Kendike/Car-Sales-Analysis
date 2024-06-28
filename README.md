# Car-Sales-Analysis





# Query
-- Create a new Table for only desire columns
Create Table project-012022-363821.Project.New_Cars_Data_Set as
SELECT `Purchase Date` , Vehicle, `P PRICE`, `TOTAL COST`,`SALE PRICE`,PROFIT, `%`, `SALE DATE`,
 FROM `project-012022-363821.Project.New_Car_Data` 

 --
-- Changed the field names and Remove Duplicates 
SELECT Purchase_Date,Purchase_Price,
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
 FROM `project-012022-363821.Project.New_Cars_Data_Set`)

--Remove Rows with empty cells 
WHERE
Purchase_Date IS NOT NULL AND Vehicle IS NOT NULL AND Purchase_Price IS NOT NULL
AND Total_Cost IS NOT NULL AND Sale_Price IS NOT NULL AND Profit IS NOT NULL AND
Percentage_Profit IS NOT NULL AND Sale_Date IS NOT NULL
