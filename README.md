# Maven-Toy-Store-Analysis

# About this project

# Maven Toys Analysis

Sales analysis of the Maven Toys Chain Stores in Mexico, using SQL and Power BI.

# Overview

We have been provided with sales & inventory data for a fictitious chain of toy stores in Mexico called Maven Toys, including information about products, stores, daily sales transactions, and current inventory levels at each location.


The data spans from January 1st, 2017 to September 30th, 2018, containing over 820,000 transactions for all stores owned by Maven Toys.


The objective is to prepare the data, analyze and visualize it, and subsequently outline findings that allow the toy store chain to enhance its decision-making capabilities and boost profits.


# The major questions that we will attempt to answer are:


Which product categories drive the biggest profits? Is this the same across store locations?
Are there any seasonal trends or patterns in the sales data?
Are sales being lost with out-of-stock products at certain locations?
How much money is tied up in inventory at the toy stores? How long will it last?

# Data Collection
     The data used within this project is provided from the following link:

           https://app.mavenanalytics.io/guided-projects/7#dataset

We are given four tables in CSV format which contain the following fields:

# Products (35 unique products)

Product_ID - Unique ID given to each product offered

Product_Name - Unique name given to each product offered

Product_Category - Category group assigned to each product based on its characteristics/utility

Product_Cost - Expense incurred for making/attaining the product, in US dollars

Product_Price - Price at which the product is sold to customers, in US dollars

# Stores (50 different stores)

Store_ID - Unique store ID given to each toy store

Store_Name - Unique store name given to each toy store

Store_City - City in Mexico where the store is located

Store_Location - Classification of location in the city where the store is located (Downtown, Commercial, Residential, Airport)

Store_Open_Date - Date when the store was opened

# Sales

Sale_ID - Unique Sale_ID for each transaction conducted in a store

Date - Date on which the transaction occurred

Store_ID - Unique store ID given to each toy store

Product_ID - Unique ID given to each product offered

Units - No of units of the product sold

# Inventory:

Store_ID - Unique store ID given to each toy store

Product_ID - Unique ID given to each product offered

Stock_On_Hand - Stock quantity of the product in the store

# Skills demonstrated

# Tool used: Microsoft Power BI. The following skills and concepts were applied through out this project:

# Data cleaning and transformation in Power Query

# Data modeling

# Data Analysis Expressions (DAX) codes

# Data visualization

# Project documentation

# The analysis process

    This is an iterative roadmap undertaken to ensure the accuracy of results and a comprehensive analysis. For this project, I am using 
    Microsoft Power BI.

# Data importation

I imported all the CSV files provided into my Power BI workspace, after which I opened them individually in Power Query to carry out data cleaning.

# Data profiling and cleaning 🧹

Data profiling is crucial as it provides a comprehensive understanding of the quality, structure, and relationships within a dataset, ensuring that potential issues are identified early on. Cleaning the data is equally vital to enhance accuracy, eliminate inconsistencies, and maintain the integrity of the information, ensuring reliable insights and informed decision-making.


# In power query, I carried out the following tasks:


Promoting headers to ensure appropriate column names.

I converted the data types of the id columns in each table from whole numbers to text since they are identifiers and would not be used for calculations.

I added three new columns, total product cost, total product price, and profit, to the sales dataset.

I double-checked the column data types and converted the wrong data types to the appropriate data types.

I trimmed the names of the stores in the stores table to reduce redundancy and create explicit and easy-to-read store names.

Furthermore, I created a Dates table that would serve as my primary date table for this analysis. I did this using the CALENDARAUTO() function, which creates a Date table by assessing the earliest and latest date in all of my tables. From this date table, I extracted the year, quarter, month, and day.

# Data modeling
Data modeling is crucial in Power BI analysis because it structures and organizes raw data into a coherent framework, enabling relationships and hierarchies that form the foundation for insightful visualizations. For this analysis, Power BI automatically connected related tables, resulting in a star schema model.

# Data Preparation:
Given the nature of the information provided, it is beneficial to place it into a MySQL database. The data has been separated into multiple tables that can be linked to each other based on identical fields. Queries provide for quick and easy manipulation of data and access to useful database insights. The usage of a database also guarantees a level of data integrity based on the enforced data types within our tables. Establishing constraints such as primary and foreign keys also allows us to avoid incorrect values and duplicated data which gives us confidence that the data we are using is accurate.

# Data Model
MavenToys Database Schema Repository in MySQL

The following trends and patterns were observed:

The month of December generated the most revenue. The month being a festive season brings with it lots of occasions and celebrations, including Christmas and Boxing Day, among others.
There was a noticeable dip in the month of August for both years. This can be attributed to the season when parents are more focused on back-to-school supplies and preparations for their kids. This month, parents prioritize purchasing school supplies, clothing, and other essentials over toys during this period.
For both years, January was off to a slow start, though not as low as that of August. This can be attributed to post-holiday lulls and budget constraints as consumers become more budget conscious and recover from holiday expenses, thereby leading to reduced spending on non-essential items, in this case toys.
Between April and June, there is an almost steady revenue generation rate. This is so because these months coincide with spring and early summer in many regions. During this time, people often engage in outdoor activities, leading to an increased demand for outdoor toys and recreational products. Also, many schools have spring breaks during these months, leading to increased family activities and potential purchases of toys for entertainment during the break.
I also observed that in 2017, after the August dip, sales steadily began climbing in the ember month until the end of the year.
Recommendations

Based on the patterns observed above, I would recommend the following to the Maven Toys management team:

An expansion into educational toy categories, for example - jigsaw puzzles, building blocks, STEM kits, coding toys, etc. This would encourage parents to invest in these toy categories to help their kids development, especially during the school year.
Collection of data on consumers in order to analyze customer spending habits and consumer behavior, customer lifetime value (CLV), churn and retention rate
A feedback form should be sent regularly on a month-by-month basis to keep track of customers preferences as the months pass by.
What is our market penetration? That is, how many stores and cities are we currently in?

2017 till date Maven Toys has a total of 50 stores spread across 29 cities.

# Market penetration

58% of stores are located in downtown areas, 24% in commercial areas, 12% in residential areas, and 6% around airports.

# Stores per location

    Is there a relationship between the number of stores in a city and the revenue generated there?

Yes, there is. There is a strong positive correlation between the number of stores in a city and the revenue generated in that city. This means that as the number of stores in a city increases, the amount of revenue generated increases as well. It is important to note that there may be a hidden variable that can affect the amount of sales generated in the stores in each city.

Relationship between number of stores in a city with revenue generated

# Recommendations

While the strong positive correlation between the number of stores in a city and the revenue generated is a valuable insight, it's prudent to consider potential confounding factors that might influence this relationship. I recommend that the following factors be considered and analyzed:

Population Density: Cities with a higher population density may naturally support more stores and higher sales due to a larger customer 
base.

Economic Factors: The economic health of a city, including factors like income levels, employment rates, and overall economic stability, can significantly impact consumer spending. Wealthier cities might have higher sales potential.

Competition: A city with a high concentration of toy stores may experience saturation, affecting the revenue generated by each store.

Local Trends and Preferences: Consumer preferences and cultural trends can vary by region. Adapting product offerings to align with local preferences is crucial for success. Consider factors such as popular toy trends and cultural influences.
Location of Stores Within Cities: The specific location of each store within a city (e.g., proximity to popular attractions, accessibility, foot traffic) can significantly influence its performance.

Operational Efficiency: Assess the operational efficiency of each store. Factors such as inventory management, staff training, and store layout can influence the customer experience and, consequently, sales.
Next steps and other recommendations

Marketing and Promotion Efforts: Variances in marketing strategies and promotional efforts among different cities can affect sales. Further analyses on the effectiveness of marketing campaigns and how they contribute to revenue generation should be made
Conduct a pilot testing experiment to assess the effectiveness of customers placing orders on the Maven Toys website, considering factors such as the cost of product shipments, packaging, and related expenses.
GitHub Link Repository: https://github.com/rupalxxiii/Maven-Toy-Store-Analysis
