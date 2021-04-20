![header_pic](images/shop.png)

# Big Shopp Sales Analysis

#### Table of Contents  

* [Project Overview](#project-overview)
* [Big Shopp Store Report](#big-shopp-store-reports)
* [Data Source and Database](#Data-Source-and-Database)
* [Interactive Dashboards](#Interactive-Dashboards)
* [Summary](#summary)

## Project Overview
This project aims to analyze the Big Shopp's Store Sales data  I have been hired to create reports to identify the total sales, the maximum sales quantity and the average saless quantity for each product category
Product categories are Audio, Home appliances, Cell phones, Computers etc... The manager also wants me to create a model where I can select a continent to indicate
the sales for that continent.

#### DAX Measures for the FactSales Table
	- Sum Sales = SUM(Sales[SalesAmount])
	- Max Sales Quantity = MAX(Sales[SalesAmount])
	- Min Sales Quantity = MIN(Sales[SalesAmount])
	- Ave Sales = AVERAGE(Sales[SalesAmount])
	- All Product Sales = CALCULATE([Sum Sales],ALL('Product'))
	- Product Sales Ratio = DIVIDE([Sum Sales],[All Product Sales],BLANK())

#### Calculated Column
	- Month = FORMAT([Datekey], "MMMM")
	- Quarter = "Q" & FORMAT(QUARTER([Datekey]), "")
	- Weekday = FORMAT([Datekey], "dddd")
	- Year = FORMAT([Datekey], "yyyy")
	- TimePeriod = 'Date'[Year]&" "&[Quarter]

## Big Shopp Store Reports
	- Total Sales by Quarter and Year.
	- Cards for: Sum sales, Max and Min Sales Quantity, & Average Sales.
	- Product Subcategory annual total sales
	- I will also include a two slicers, the first one you can select the 'Product Category'.
	- The second one you can select which continent the sales origenated from.

## Data Source and Database
- Microsoft Access Store Sales database

## Interactive Dashboards
- Please visit our [visual dashboard](https://app.powerbi.com/groups/me/reports/f406054b-a18f-492f-8934-274662428865/ReportSection?noSignUpCheck=1&redirectedFromSignup=1&ScenarioId=signup)

## Summary
In this project we analyzed the Big Shoop sales data. We created a dashboard the store. We started off by creating groups 
