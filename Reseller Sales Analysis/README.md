![header_pic](images/bike.png)

# Reseller Sales Analysis

#### Table of Contents  

* [Project Overview](#project-overview)
* [Sales Analysis Visuals](#Sales-Analysis-Visuals)
* [Data Source and Database](#Data-Source-and-Database)
* [Interactive Dashboards](#Interactive-Dashboards)
* [Summary](#summary)

## Project Overview
In this project, I work for a bike equipment company and I have been asked to analyze the sales data. I am required to compare monthly store sales against 
specific calendar years. For this comparison I will have to select the reseller's business type, which includes a Specialty Bike Shop, a Value Added Reseller and a Warehouse.
For this comparison I will create measures that only includes resellers who have been in business for at least a year at the time of the sales. 
To accomplish this I would create DAX measures and calculated columns to return the required data. 

#### DAX Calculated Columns
Using the DAX RELATED function,  I will create a calculated column in the Product table for Product Subcategory and Product Category. If the ProductSubcategoryKey is blank,I will fill in
the Category and Subcategory columns with "Misc".. I will Use the ISBLANK function for this

	- [Category]
  	=IF(ISBLANK([ProductSubcategoryKey]),"Misc",
  	RELATED(Category[EnglishProductCategoryName]))

	- [Subcategory]
  	=IF(ISBLANK([ProductSubcategoryKey]),"Misc",
 	 RELATED(Subcategory[EnglishProductSubcategoryName]))

- Finally, I will create a hierarchy with the Product Category and Product Subcategory columns named Prdoduct Category. 

#### DAX Measures for the Sales Table
	- Month Sales:=TOTALMTD(SUM([Sales Amount]),'Date'[Full Date])
	- Prev Month Sales:=CALCULATE(Sum([Sales Amount]),PREVIOUSMONTH('Date'[Full Date]))
	- Monthly Sales Growth:=[Month Sales] - [Prev Month Sales]
	- Monthly Sales Growth %:=DIVIDE([Monthly Sales Growth],[Prev Month Sales],0)
	- Month Sales Filtered:=Calculate([Month Sales],FILTER(Reseller,[Was Open Prev Year]=1))
	- Prev Month Sales Filtered:=CALCULATE([Prev Month Sales],Filter(Reseller,[Was Open Prev Year]=1))
	- In each measure change value to Currency with 2 decimal points 
        - % Sales Growth change value to percentage with 2 decimal places

## Sales Analysis Reports
- Final table includes Product category and sub category, reseller’s monthly sales, monthly sales filtered, the previous month sales and the previous month sales filtered
- A clustered Column chart and a slicer indicating the Reseller’s business type would also be in my report along with a KPI indicating the monthly sales by year

## Data Source and Database
- Microsoft Access StoresSales database

## Interactive Dashboards
- Please visit our [visual dashboard](https://app.powerbi.com/groups/me/reports/a78986b8-079b-4acd-a024-fd4740b255c3/ReportSection?noSignUpCheck=1&redirectedFromSignup=1&ScenarioId=signup)

## Summary
In this project I analyzed the sales data for a bike company. I compared monthly store sale against the 2013 to 2016 calendar year.  Monthly stores sales was compared to the different business types. The resulting dashboard indicated a KPI’s showing the monthly sales by year figures and a bar chart showing the calendar year monthly sales.


