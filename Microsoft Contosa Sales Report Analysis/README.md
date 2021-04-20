![header_pic](images/electronics.png)

# Microsoft Contosa Sales Data Analysis

#### Table of Contents  

* [Project Overview](#project-overview)
* [Gross Profit Models](#gross-profit-models)
* [Budget Sales Reports](#budget-sales-reports)
* [Data Source and Database](#Data-Source-and-Database)
* [Interactive Dashboards](#Interactive-Dashboards)
* [Summary](#summary)

## Project Overview
This project aims to analyze the Contosa sample data from Microsoft.  Contosa is an electronics company that sells various products through stores, online and resellers. This model contains 
sales data from 2007 to 2009. In this scenario, I work with a company that analyzes Contosa’s 'Gross Profit' from different dimensions and the annual Bundget & Sales Amount totals. 
I am going to analyze the data using various dimensions including DimProduct, DimProduct Subcatogery & DimPromotion.

#### Grouping
In this project we are going to create a new group called BrandName from the DimProduct table using the field BrandName.  Under this group we will utilize the brands: AdventureWorks, Contosa and Northwind Traders .

#### DAX Measures for the FactSales Table
	- % Items Returned = SUM(FactSales[ReturnQuantity])/ SUM(FactSales[SalesQuantity]) 
	- Discount % = FactSales[DiscountAmount]/FactSales[SalesAmount] 
	- GP % = [Gross Profit]/SUM(FactSales[SalesAmount]) 

#### Calculated Column
	- Discount % = FactSales[DiscountAmount]/FactSales[SalesAmount] 

## Gross Profit Models
	- Line chart for our Gross Profit period.
	- Clustered colum chart for our Gross Profit Channel Name and Class Name (Deluxe, Economy and Regular).
	- Clustered bar chart for Gross Profits by Brand Name.
	- Clustered bar chart for Gross Profit by Subcategory Name (Camcorders, Projectors, Digital Cameras, etc...).
	- Scatered chart for Sales Amount and GP Sales Quantity showing the gross profit over time.
	- I will also include a two slicers, the first one you can select the 'FiscalYear' and the second one you can 'Choose Brand'.


## Budget Sales Reports
	- A slicer to indicate the 'CalendarYear' 2007, 2008, & 2009.
	- A Budget & Sales Amount by Month table with the following columns: CalendarMonth, BudgetAmount, SalesAmount, & BrandName.
	- KPI trend over time, the trend over time I would be measuring is BudgetAmount.
	- Muli-row card to see if we are behind, infront and by how much in sales. This would be the BudgetAmount Vs SalesAmount
	- Clustered column chart for Budget Amount, & Sales Amount stacked by Brand Name.


## Data Source and Database
- Microsoft Contosa Sales Data

## Interactive Dashboards
- Please visit our [visual dashboard](https://app.powerbi.com/groups/me/reports/e141dac2-be8d-445a-8a28-d145aade080e/ReportSection?noSignUpCheck=1&redirectedFromSignup=1&ScenarioId=signup)

## Summary
In this project we analyzed the Contosa sample data from Microsoft using the Microsoft Contosa Sales Data. We created two dashboards one for the Gross profit Models
and one for the Budget Sales Models. We started off by creating groups for the brands: AdventureWorks, Contosa and Northwind Traders. We then added a calculated column 
to show the percentage discount for the sales anmount. Other stepa included were creating DAX measures for discount percentage and gross product (GP) percentage.
