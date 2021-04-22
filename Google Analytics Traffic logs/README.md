![header_pic](images/WebAnalytics.png)

# Google Analytics Traffic Reports

#### Table of Contents  

* [Project Overview](#project-overview)
* [Data Source and Database](#Data-Source-and-Database)
* [Interactive Dashboards](#Interactive-Dashboards)

## Project Overview
This project aims to analyze Google Analytics Traffic logs metrics. In this scenario, I work with a company that analyze web traffic movements and I have
been asked to analyze the traffic logs metrics. The first metric that I want to analyze is the total web traffic visits, which is the total visit counts.
- I am going to look at visits over time using a line chart utilizing visit count and date columns.
	- By selecting any month the dispay returns the total visits for that selected month.
- I will look at the internet traffic bounces, this is when a visitor visits your webpage. We will add the bounces column and then change chart type to line and clustered chart
	- The resulting chart would indicate the number of bounces of each month selected.
- I am going to look at the split between new and returning visitors. The visitor type would be 'New Visitors' Vs 'Returning Visitors'
	- To accomplish this I am going to create a pie chart comparing the visit count to visitor type.
- Next I am going to look at our website traffic sources. I am going use a clustered bar chart and for the fields we are going to select the source and visit count columns.
	- The resulting clustered bar chart would return the the visit count by source; source can be Google, Bing... etc.
	- I added a line chart to show the length of time a visitor stays on a website and by the date they visited.
- Finally I want to see where our visitors are coming from. I am going to use a filed map chart and the fields are the country and visit count columns.
	- The lighter the color the higher the count with highest visitor count located in the United States.

## Data Source and Database
- Google Analytics website traffic excel file

## Interactive Dashboards
- Please visit our [visual dashboard](https://app.powerbi.com/groups/me/reports/ecee17ed-a02d-408f-9213-1d1d7538f119/ReportSection?noSignUpCheck=1&redirectedFromSignup=1&ScenarioId=signup)

## Summary
In this project I analyzed Google Traffic logs metrics. To accomplish this task of analyzing web traffic movements and traffic logs metrics, I created a dashboard showing   the total visit count and bounces of web traffic. I created a horizontal slicer whereby you can select all months or only just a single month. In the dashboard you can also see the percentage of new vs returning visitors and the visitor’s country. From the map you are able to read the tool tip showing the selected country’s count. The lighter the region, the higher the country’s count was.
