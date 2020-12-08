# Northwind Dashboard
This project was completed in week 6 of the Data Science Bootcamp at SPICED Academy in Berlin. The goal is to build a dashboard on top of a Postgres database that runs in the AWS cloud.

## Description
The Northwind database is a sample database created by Microsoft for tutorials and testing purposes. It contains information about the business of *Northwind Trades*, a fictional company that sells various food products internationally. It includes information about orders, inventory, purchasing, suppliers, shipping, and employees. 

For this project, I got the data in the form of several .csv files from [here](https://github.com/pawlodkowski/northwind_data_clean). Additionally, I got a .csv file from [here](https://datahub.io/core/country-list) containing country names and their ISO_A2 codes, in order to plot data on a world map. The data was imported into a local Postgres database, then hosted on AWS RDS and EC2, which is connected to Metabase to run continuously. 

You can read more about the project workflow in [this blog post](https://lorenaciutacu.com/2020/11/06/week-6-datasciencebootcamp/).

## Dashboard
The dashboard was created in Metabase and represents KPIs on the Sales and Team of *Northwind Trades*. 
- The SALES part includes data from the Orders and Products tables.
- The TEAM part includes data from the Employees, Customers, and Orders tables.

![dashboard_demo](https://github.com/spicedacademy/stochastic-sage-student-code/blob/lorena/week_6/dashboard_demo.gif)

## Files
- [`northwind_database.sql`](https://github.com/lorenanda/northwind-dashboard/blob/main/northwind_database.sql): code dump for PostgreSQL to create the tables.
- [`northwind_queries.sql`](https://github.com/lorenanda/northwind-dashboard/blob/main/northwind_queries.sql): queries used for creating the dashboard KPIs
- [`northwind_queries.py`](https://github.com/lorenanda/northwind-dashboard/blob/main/northwind_queries.py): same queries, but integrated with SQLAlchemy and pandas.
- [`dashboard_demo.gif`](https://github.com/spicedacademy/stochastic-sage-student-code/blob/lorena/week_6/dashboard_demo.gif): recorded dashboard interaction.
