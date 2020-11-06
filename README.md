# Northwind Dashboard
This project was completed in week 6 of the Data Science Bootcamp at SPICED Academy in Berlin. The goal is to build a dashboard on top of a Postgres database that runs in the AWS cloud.

## Description
The Northwind database is a sample database created by Microsoft for tutorials and testing purposes. It contains information about the business of *Northwind Trades*, a fictional company that sells various food products internationally. It includes information about orders, inventory, purchasing, suppliers, shipping, and employees. 

## Setup
For this project, I got the data in the form of several .csv files from [here](https://github.com/pawlodkowski/northwind_data_clean). Additionally, I got a .csv file from [here](https://datahub.io/core/country-list) containing country names and their ISO_A2 codes, in order to plot data on a world map. The data was imported into a local Postgres database, then hosted on AWS RDS and EC2, which is connected to Metabase to run continuously. You can read more about the project workflow in [this blog post](https://lorenaciutacu.com/2020/11/06/week-6-datasciencebootcamp/).

## Dashboard
The dashboard was created in Metabase and represents KPIs on the Sales and Team of *Northwind Trades*. 
- The SALES part includes data from the Orders and Products tables.
- The TEAM part includes data from the Employees, Customers, and Orders tables.

You can find some of the queries used for creating these KPIs in the [`northwind_queries.py` file](https://github.com/lorenanda/northwind-dashboard/blob/main/northwind_queries.py).

![dashboard_demo](https://github.com/spicedacademy/stochastic-sage-student-code/blob/lorena/week_6/dashboard_demo.gif)

## Improvements
Pretty as it may be, the dashboard has some flaws/bugs, which I hope to fix eventually:
- Filters (date, quarter, country) are not applied to all represented data.
- Map representation of cities is not working. This is because the dataset does not inlcude the latitude and longitude coordinates of the cities. 
- Photos of employees are broken, the path is not valid.
