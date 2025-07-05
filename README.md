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
   - 🧹 **Data Type formatting:** The data Type for each of the 21 attributes were ensured they are the correct data type. The order_id was changed to VarChar and made the primary key, order_date in DATE, sales, shipping_cost, discount, unit_price and profit in decimal (10,2) data Type.


