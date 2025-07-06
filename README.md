# SQL-KMS-file_Documentation

A SQL-based analysis of Kultra Mega Stores (KMS) specialist in office supplies and furniture order data from 2009 to 2012.

## 📖 Project Topic: Comprehensive Business Intelligence Analysis for Kultra Mega Stores (2009 - 2012).


### 🔭 Project Overview

This Data analysis project aims to analyze the Kultra Mega Stores order data from 2009 to 2012 to support the Abuja division of Kultra Mega Stores. The analysis focuses on identifying top-performing product categories, regions and customers, evaluating shipping methods and order prioritization, customer segmentation, and return patterns. The goal is to provide actionable insights to improve profitability and operational efficiency. 


### ✍️ Dataset Description

- **Source**: The data was provided by the incubator hub for the purpose of the hackathon and final Examinations of my data analysis program by the organization. The dataset contains two .csv files information scraped from 2009 to 2012, including: 
   - **KMS orders Table:** Containes 8,400 records of orders with 21 ttributes including 
     - Order details: Order_ID, Order dates, price and quantities 
     - Customer information: Names, Province, segment and Region
     - Product details: category, sub-category, name, container, base margin, etc.
     - Financial metrics.
   - **Order_Status Table:** Contains 573 records of returned orders. Each record has an order_id nd the status 'returned'. Orders not present in this table are considered not returned. 

 ### 🧰 Tools Used
 
   1. Microsoft Structured Query Language (SQL) Server Management Studio (For database management and query execution)
   2. Github Markdown for documentation in the repository.

### 🧑‍🔬 Methodology 

In the initial phase of the data cleaning and preparation, the following actions were performed;
   - ⏳ **Data Acquisition and inspection:** The data was loaded and the total number of records and fields were confirmed to be the same from the source.
     
   - 🔃 Data Import: The two .csv data were imported by right-click on the database, then  task and navigate to import flat file.
     
   - 🧹 **Data Type formatting:** The data Type for each of the 21 attributes were ensured they are the correct data type. The order_id was changed to VarChar and made the primary key, order_date in DATE format, sales, shipping_cost, discount, unit_price and profit in decimal (10,2) data Type. The order_id consistency between datasets was also ensured.
     
   - SQL schema and Setup

A schema; a logical container that organizes database objects (tables, views, etc) was setup. The default schrms dbO (Database Owner) was used [dbo].[KMS] was used.


### 💹 SQL Analysis

The key business questions were answered by writing some structured query language



### 🔑 Key Findings & Insights:

**Case scenariio I:**
1. Which product category had the highest sales?
   - The sales by product_category was sum up, ordered and the top one was picked.
   
2. What are the Top 3 and Bottom 3 regions in terms of sales?
   - The sales was sum up by region, then ordered to select the top 3 and bottom 3 as shown in the query written below:
   
3. What were the total sales of appliances in Ontario? 
   - Filter by product_category = 'Appliances' and province = 'Ontario' then sum sales.
4. Advise the management of KMS on what to do to increase the revenue from the bottom 10 customers. 
   - The bottom 10 customers by total sales was identified, the advice were given based on the output of the query.
     
5. KMS incurred the most shipping cost using which shipping method?
   - The shipping_cost was sum up by ship_mode and the top 1 was filtered.

**Case Scenario II:**

6. Who are the most valuable customers, and what products or services do they typically purchase? 
   - Most Valuable customers was defined by the total profit and the common product_categories they bought were also listed.

7. Which small business customer had the highest sales? 
   - The Customer_segment was filtered as = 'small Business', then sum sales by customer_name and ordered by sales in descending order to get the top customer.


8. Which Corporate Customer placed the most number of orders in 2009 – 2012? 
   - The order_id was counted distinctly by customer_name for customer_segment = 'corporate' and the top 1 was gotten.


9. Which consumer customer was the most profitable one? 
   - The Customer_segment was filtered as = 'Consumer', then sum sales by customer_name and ordered by sales in descending order to get the top customer.


10. Which customer returned items, and what segment do they belong to? 
    - full outer join order_status (where returned status = 'Returned') with orders to get the customer_name and their segment.


11. If the delivery truck is the most economical but the slowest shipping method and  Express Air is the fastest but the most expensive one, do you think the company appropriately spent shipping costs based on the Order Priority? Explain your answer


### 💡 Strategic Recommendations and Conclusion
   1. Cap Discountst 40% for 


## 🗝️ Key Performance Indicator (KPIs)
   - Total Number 
