# Superstore-Retail-Business-Analysis-Using-Power-BI

Case Study

A superstore retail business is a large, multi-department store that sells various products, including
groceries, electronics, home goods, clothing, and more. These stores are often designed to be a one-stop
shop for customers, offering a wide range of products and services under one roof. Superstores are
typically larger than traditional retail stores and may have a larger product selection. Superstores are
often part of a larger chain and have multiple locations in a region or country.
A new store manager needs your help to better understand his/her Data Operations Team. You are
provided with part of the sales data that a Business Intelligence Analyst encounters daily. Design the
dashboard to analyze and interpret the data to help provide valuable insights to the store manager.

Dataset

A Superstore dataset typically includes information about the products, customers, and sales associated
with a retail store. It may include the following columns:

Table Description:-
Sl.No Column Name Column Description

1 Order ID:- Unique Identifier For the Order

2 Order Date:- Date of the order placed

3 Ship Date:- Date of the order shipped

4 Ship Mode:- Priority Mode of Shipping ( Same Day, First Class, Second Class, Standard Class )

5 Customer ID:- Customer Unique Identifier

6 Customer Name:- Name of the customer

7 Segment:- Customer Segment ( Consumer, Corporate, Home Office )

11 Postal Code:- Address from the order was placed

12 Region:- Name of the Region

13 Product ID:- Unique product identifier

14 Category:- Product category 

15 Sub-Category:- Product Sub-Category
16 Product Name:- Name of the product
17 Quantity:- Quantity of the product ordered
18 Discount:- Discount % on the product
19 Buy Price:- Buying price for each item
20 Price Per Each:- Selling price for each item 



Problem Statement:-
Data Extraction, Cleaning,Loading and Transformation

1. Desk representatives at the stores are not tech savvy hence they directly share the data in the single
excel file. As a Power BI Developer, read the data directly from the excel file.

2. The data coming from the source is in raw form in the flat file; hence clean and prepare (transform) the
dataset for efficient use. Delete the empty columns and rows, change the fields to appropriate data types
and split the fields and rename the columns appropriately.

3. Standardize the values in the column Ship mode [Hint: Replace FC with first class]

4. Split the address column to City, State, Country and Pincode

Data Modeling:-

1. Tracking sales in the retail business is a weekly task; hence setting up the data model will be crucial for
this. Convert a flat file into STAR schema for better performance of the analysis. The schema shall have a
central Fact table, ‘Orders’ and three dimension tables,’Order details’, ‘Customer’ and ‘Product’. Refer to
the table below for creating appropriate columns in each table.

2. Remove duplicate rows from the newly created dimension tables, and ensure there are no empty rows

3. Once the tables are created, ensure one- to - many relationships are created between dimensions and
fact table.

Column Name Type:-

Ship Mode Dimension(Order Details)
Postal Code Dimension(Order Details)
Region Dimension(Order Details)
Customer ID Dimension (Customer)
Customer Name Dimension (Customer)
Segment Dimension (Customer)
Product ID Dimension (Product)
Category Dimension (Product)
SuPb-Category Dimension (Product)
rev Complete & Continue 


Data Analysis:-
Furthermore, to grow the footholds in the store and achieve an ambitious sales target, the store manager
wants to track and visualize the following metrics.

1. Create a new column ‘Sales’ or ‘Order value’ [Hint: Sales = Qty*price per qty*(1- % Discount)]. Create a
card visual displaying the total sales.

2. Similarly calculate the Sales from discounted products and display the total sales from discounted
products.

3. Since supermarkets sell bulk items, store managers want to know each order's cart value. Create a
column “Cart Value” that categorizes the order value/sales as Low, medium, high or very high.
Cart Value,
< 1000: Low
<3500: Medium
< 10000: High
> 10000: Very High
[Hint : From Power Query editor->Add column-> Conditional column OR
DAX formula using nested IF( ) function]
Create a pie chart with Cart value as legend and Order value in Values field.

4. Separately visualize the total sales just from the low cart value category (as mentioned, any value below
1000 can be considered as low value category).

5. Using card visual, track the total sales coming from the low cart category and discount more than or
equal to 50% to find out the contribution and cause.
[Hint: Create a new measure, sales using calculate() and sum() function with the two filters, Low cart
category and discount>=50% OR calculate sales using sumx() with if() and and()]
Prev Complete & Continue Next

6. Find out the number of days it takes to deliver for each shipment type (refer ship mode) so that delivery
issues can be looked at on priority [Hint: No of days to deliver can be calculated from the difference
between order_date and shipping_date]. Create a column chart that shows the average number of days
it takes to deliver for each shipment type.

7. So far the store manager has managed to see the current snapshot of the sales based on various
criteria. In the Retail business, do we see a spike in sales on special occasions like festivals? To achieve this,
create a matrix visualization that displays order date as hierarchy , sales and sales year to date.

8. Visualize the cumulative sales for each month for all the years to calculate Year on Year Sales Growth.
Calculate YoY growth.
