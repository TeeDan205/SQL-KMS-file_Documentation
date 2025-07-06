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
       
   - **Order_Status Table:** Contains 573 records of returned orders. Each record has an order_id and the status 'returned'. Orders not present in this table are considered not returned. 

 ### 🧰 Tools Used
 
   1. Microsoft Structured Query Language (SQL) Server Management Studio (For database management and query execution)
      
   2. Github Markdown for documentation in the repository.

### 🧑‍🔬 Methodology 

In the initial phase of the data cleaning and preparation, the following actions were performed;
   - ⏳ **Data Acquisition and inspection:** The data was loaded and the total number of records and fields were confirmed to be the same from the source.
     
   - 🔃 **Data Import:** The two .csv data were imported by right-click on the database, then  task and navigate to import flat file.
     
   - 🧹 **Data Type formatting:** The data Type for each of the 21 attributes were ensured they are the correct data type. The order_id was changed to VarChar and made the primary key, order_date in DATE format, sales, shipping_cost, discount, unit_price and profit in decimal (10,2) data Type. The order_id consistency between datasets was also ensured.
     
   - 🛠️ **SQL schema and Setup:** A schema; a logical container that organizes database objects (tables, views, etc) was setup. The default schema dbO (Database Owner) was used [dbo].[KMS] was used.


### 💹 SQL Analysis

The key business questions were answered by writing some structured query language

**Case scenario I:**
1. Which product category had the highest sales?
    **The Highest-Selling Category** was obtained by writing the below query:
     
   ![1qry REAL](https://github.com/user-attachments/assets/6494816d-fa85-4303-9248-3ebb71cd86ed)
   
   - The sales by product_category was sum up, ordered and the top one was picked.

   **Query Result:**

   ![1 ansa REAL](https://github.com/user-attachments/assets/e8297778-060a-488f-baa4-f74c21dc4e01)

   **Key Insight:**
   Technology products generated 42% more revenue than secon-place Furniture ($1.3M), indicating strong market demand for electronics.
   
2. What are the Top 3 and Bottom 3 regions in terms of sales?
     **The Top 3 Regions** were obtained by writing the query (ranked in descending order) as shown below:

    ![2qry](https://github.com/user-attachments/assets/6ad326f9-bc17-47cd-bdde-e4b07b49e146)

    **Query Result:**

    ![2a Ansa](https://github.com/user-attachments/assets/8cfe621f-4dc0-4c48-aaa4-bbd9fb1c06da)

      **The Bottom 3 Regions** were obtained by writing the query (ranked in ascending order) as shown below:

    ![2b qry](https://github.com/user-attachments/assets/a5739c21-c4c5-4f76-a971-926f4a0291c6)

    **Query Result:**
   
    ![2b ansa](https://github.com/user-attachments/assets/48c86a70-cfc9-4962-a969-0410c8ab5b21)

     **The Top/Bottom 3 Regions** in terms of sales are shown in the queries results shown above.
   
   - The sales was sum up by region, then ordered *appropriately* to select the top 3 and bottom 3.
   
4. What were the total sales of appliances in Ontario? 

    **The Total Sales of Appliances in Ontario is found by writing the query below:**

    ![3 qry](https://github.com/user-attachments/assets/a13314ef-550e-4bcf-8e83-0343d1036d38)

    **Query Result:**

     ![3](https://github.com/user-attachments/assets/534926b6-15b3-406c-8348-bcf9db772d1b)

     The Appliances Sales in Ontario is **$202,346.84**

   - Filter by product_category = 'Appliances' and province = 'Ontario' then sum sales.

5. Advise the management of KMS on what to do to increase the revenue from the bottom 10 customers. 

   **Revenue Growth for Bottom 10 Customers** query was written as shown below:

    ![4](https://github.com/user-attachments/assets/894f0c4b-5394-4482-8a69-df2464ae7df6)

    **Query Result**

    ![4ansa](https://github.com/user-attachments/assets/d7d40274-f465-4878-98ec-dbe4914ac3dd)

     Having identified the bottom 10 customers in terms of sales, region and  their prefrences;

   (i) Create a branch closer to Alberta Province and those far away region from the Kuga Mega Store location.

   (ii) Reduce discounts for chronic low-margin customers

   (iii) Increase the shipping cost for low order quantities

   (iv) Enforce shipping minimums or add surcharges for small orders.

   (v) Understand the reason for returning some orders and tackle it immediately.

   - The bottom 10 customers by total sales was identified, the advice above were given based on the output of the query.
     
6. KMS incurred the most shipping cost using which shipping method?

    **The Hishest Shipping Cost Method** is found by using the SQL:

      ![5qry](https://github.com/user-attachments/assets/9364bbf4-8c0d-4b44-9dea-2f1d27dc5bff)

    **Query Result:**

      ![5nsa](https://github.com/user-attachments/assets/8188903f-fb8c-4af7-8dd5-f293c1eeb659)

 **The Hishest Shipping Cost Method** is **Delivery Truck** with a total shipping cost of **$51971.94**
   - The shipping_cost was sum up by ship_mode and the top 1 was filtered.

**Case Scenario II:**

6. Who are the most valuable customers, and what products or services do they typically purchase? 

    **The Most Valuable Customers & Preferences** was obtained by writing the below query:

      ![6query](https://github.com/user-attachments/assets/c0fab9ad-412a-4427-8419-9cc5db8b8e53)

    **Query Result:**

     ![6ansa](https://github.com/user-attachments/assets/3220fb02-99ad-4105-ad32-199e354640f7)

     **The Most Valuable Customers & their Preferences** are shown in the query result above.
       - Most Valuable customers was defined by the total profit and the common product_categories they bought were also listed.

7. Which small business customer had the highest sales? 
    - The Customer_segment was filtered as = 'small Business', then sum sales by customer_name and ordered by sales in descending order to get the top customer. The query is written as shown below:

     ![7qury](https://github.com/user-attachments/assets/90d76144-94e1-4b00-ac24-5ca4b0a3f403)

     **Query Result:**
  
     **Top small Business Customer** is **Dennis Kane** with the highest sales of **$33367.85**

8. Which Corporate Customer placed the most number of orders in 2009 – 2012? 
    - The order_id was counted distinctly by customer_name for customer_segment = 'corporate' and the top 1 was gotten. The query is written as shown below:

     ![8query](https://github.com/user-attachments/assets/833fca68-8a02-47c1-b02f-9e4d859b5acc)

     **Query Result:**
  
     **Corporate Order Leader** is **Barry Weirich** with the highest number of orders in 2009 – 2012. he ordered  **50**

9. Which consumer customer was the most profitable one? 
    - The Customer_segment was filtered as = 'Consumer', then sum sales by customer_name and ordered by sales in descending order to get the top customer. The query is written as shown below:

      ![9query](https://github.com/user-attachments/assets/6a63aa25-c771-4388-818f-df08eb975cbf)

      **Query Result:**
  
      **Most Profitable Consumer** is **Emily Phan** with a profit of **$27220.69**

10. Which customer returned items, and what segment do they belong to? 
     - full outer join order_status (where returned status = 'Returned') with orders to get the customer_name and their segment s shown in the query written below:

     ![10 to join](https://github.com/user-attachments/assets/39d0f54a-9ced-45cc-98b8-7dba0ceb4dcd)

  After the two tables were left-joined using order_id as the primary key, view of the new combined table was created and a query was written to get the customer who returned items the most.

   ![10 to ansa](https://github.com/user-attachments/assets/c3304f85-54e1-4fb2-acff-932e49a31459)

   **Query Result:**
  
   **Returning Customers & Segments** is **Patrick Jones** in the **Home Office** Customer Segemnt with  total **30** returned items.

11. If the delivery truck is the most economical but the slowest shipping method and  Express Air is the fastest but the most expensive one, do you think the company appropriately spent shipping costs based on the Order Priority? Explain your answer

    **The shipping Cost Efficiency** is obtained by using the query below:

    ![11qry](https://github.com/user-attachments/assets/2f184629-7d81-4fbc-9bbe-7651846ef143)

    **Query Result:**
 
     The company appropriately spent shipping costs based on the order priority because majority of the ship mode matched the order priority. Delivery truck was used for low and medium order priority products while the Express Air ship mode was used for high and critical order priority.


### 🔑 Key Findings & Insights:



### 💡 Strategic Recommendations and Conclusion
   1. Cap Discountst 40% for 


## 🗝️ Key Performance Indicator (KPIs)
   - Total Number 
