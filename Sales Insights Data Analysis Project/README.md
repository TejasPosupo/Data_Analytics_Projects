
# ✨ Sales Insights Data Analysis Project ✨

## Project Explanation

![Atrrition DashBoard](https://github.com/TejasPosupo/Data_Analytics_Projects/blob/main/Sales%20Insights%20Data%20Analysis%20Project/sales.gif)

Insights into Sales Data Analytics projects for brick and mortar businesses entail analysing data to get insights into consumer behaviour, product trends, and other factors that influence sales. Here are some examples of potential projects and how they can benefit a brick and mortar business.

Customer segmentation is analysing customer data to determine several categories based on demographics, purchasing behaviours, and other factors. Businesses that understand these groups may modify their marketing tactics and product offerings to better fit the demands of each group.

Store Traffic Analysis: This entails analysing consumer behaviour in-store using data from foot traffic sensors and other sources. Businesses, for example, can determine which portions of the shop are the most often frequented and which goods are the most popular. This data may be utilised to improve shop design and product positioning.

Sales forecasting entails forecasting future sales using previous sales data as well as other variables like as seasonality and economic indicators. This data may be utilised to manage inventory and employee levels, as well as define sales goals.

Product Performance Analysis is analysing sales data to determine which goods sell well and which do not. Businesses may make educated judgements regarding product development, marketing, and inventory management by spotting these patterns.

This entails analysing customer data in order to assess a client's lifetime value. Businesses may focus their marketing efforts on maintaining and attracting comparable consumers by knowing which clients are most valuable.

Sales Data Analytics projects may assist brick-and-mortar businesses in making data-driven decisions that lead to increased sales and profitability. 
Businesses may better understand their consumers and remain ahead of the competition by harnessing data to obtain insights into customer behaviour and market trends.

## Topics Covered in this Project
- Import data in Power BI
- Data Cleaning in Power BI
- Data Modelling in Power BI
- Power Query Editor
- DAX in Power BI
- Measures and Calculations in Power BI
- Charts in Power BI
- Filters and Slicers in Power BI
- Dashboard in Power BI 
- Insights from Dashboard 


## Tech Stack 💻

- PowerBI


### Instructions to setup mysql on your local computer

1. SQL database dump is in db_dump.sql file .

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Data Analysis Using Power BI
============================

1. Formula to create norm_amount column

`= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`



