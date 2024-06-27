# Car-Sales-Analysis





# Query
-- Create a new Table for only desire columns
Create Table project-012022-363821.Project.New_Cars_Data_Set as
SELECT `Purchase Date` , Vehicle, `P PRICE`, `TOTAL COST`,`SALE PRICE`,PROFIT, `%`, `SALE DATE`,
 FROM `project-012022-363821.Project.New_Car_Data` 

 --
 -- Changed the field names to remove the spaces
SELECT 
`Purchase Date` as Purchase_Date,
Vehicle,
`P PRICE` as Purchase_Price,
`TOTAL COST` as Total_Cost,
`SALE PRICE` as Sale_Price,
PROFIT as Profit,
`%` as Percentage_Profit,
`SALE DATE` as Sale_Date
 FROM `project-012022-363821.Project.New_Cars_Data_Set` 
