**🛒E-COMMERCE SALES PERFORMANCE AND RETURN ANALYSIS DASHBOARD**

**PROJECT OVERVIEW**

Despite generating 5.9M in sales across  34k Orders and a YOY growth of 52.7%,an e-commerce company was making negative returns.The total cost of goods sold exceeded the revenue also compounding this was a high product return rate which translated to further the business running at a loss.This Project shows an end-to-end e-commerce cycle that analyzes sales,product performance,customer demography,regional distribution as well as return rate overviews. 
My task was to analyze sales,identify the most returned products,highlight top selling products and also provide actionable recommendations for improving revenue and reducing product returns.

**OBJECTIVES**

• Analyze sales performanceand returns over time.

• Identify top selling products.

• Identify the most returned products.

• Analyze regional sales trend

• Understand customer's purchase behaviour.

• Evaluate return rate.



**DATASET OVERVIEW**

• Size-34485 Transactions

• Duration-Jan 2023- Dec 2025

• No of Columns-19

Created new fields like;Age_range category,transit_days range.

A date table was created for time intelligence calculations and a relationship was created with the facts table.

**TOOLS USED**

Tools used in carrying out this project were;

• Excel -Was used to perform data cleaning,fixing of missing values,eliminating duplicates and standardizing the column formats

• SQL-Was used to derive the KPI’s from the raw data

• Power BI-Was used to create some dax measures,new columns,table and display visuals that tell a story about the business.

**KEY METRICS ANALYZED**

• Total Sales: $5.9M

• Total Orders: 34,485

• Total Returns: ($308.5k)

• Return Rate %: 5.52

• Total Cost:$6.2M

• Average Order Value:  $170.0

**DASHBOARD OVERVIEW**

The PowerBI report is structured into two focused pages that is the Sales overview and the Return analysis.

<img width="1185" height="665" alt="image" src="https://github.com/user-attachments/assets/d14c09fc-3a69-4521-801b-a355d886f8a0" />

**KEY BUSINESS QUESTIONS THIS PAGE ANSWERS**

1.What is the trend of sales And cost over time?

2.What product categories are top selling?

3.Which region generates the most revenue?

4.What payment method is most preferred and used by customers?

5.What group of customers have  the greatest spending power?

**ANALYSIS AND INSIGHTS**

• The business grew in terms of volume and not profitability.Sales grew steadily from $442k in January to $543k in December.The COGS was above the sales throughout the same period which indicates that low returns was not seasonal but structural.

• There was no major break even during the year and the consistent gap between the COGS and revenue ruled out occurences like one off bad month or promotional campaign periods which simply points to pricing starategies not properly set.

• Revenue is concentrated more in the South($1.30M) and North $1.26M while the Central region$940.5k was lagging creating regional imbalance in sales.

• Electronics is the category that records the highest sales volume with a revenue of $3,32M making it the primary driver of overall growth while Grocery had the least revenue $82k

• Credit Cards(35%) and Debit Cards(25%)are the most preferred mode of payment ,this is vital for improving customer retention and conversion.

• Age group 18-43 which are predominantly the GENZ and Millenials raked in the highest revenue $1.98M with an average order value of $175k this shows they posses a high spending power followed by the Ages 55+ with a revenue of $1.6M also contributed significantly to the growth of the business.

**RECOMMENDATIONS**

• Review the pricing model across all categories by conducting a full unit economics review that will ensure products are not sold below the true landed cost per order, compare with the AOV of $170 then identify the break even point and reprice accordingly.

• Ensure stock availibilty,carrier handling agreements,packaging standarads and fast delivery are prioritised for electronics above all categories,giving that it contributes majorly to the business growth.

• Invest in marketing and promotional startegies on home and sports categories to grow both to at least $1.5M mark over the next 12months since they are stable contributors with reliable margins.This is a risk management action aiming to reduce dependency on electronics.

• Run a targeted promotion for the central region and ensure that discounts are tied to the COD and UPI payment methods which are next to the often used card payment,un;ocking more conversions from the former.Schedule deliveries for next day or 2days transit.

• Optimize and ensure zero friction on all card transactions since 60% of payment runs through that medium.Monthly audit on checkout funnel,payment gateway performance  and card authorization in order for customers to have seamless transactions.

 **RETURNS OVERVIEW**

<img width="1190" height="662" alt="image png (1)" src="https://github.com/user-attachments/assets/66fc878c-0af4-472b-b01f-d01893796d5e" />

 **KEY BUSINESS QUESTIONS THIS PAGE ANSWERS**

1.What product category was being returned the most?

2.What region experienced the return of products and what category was being returned?

3.On what transit day did the return rate spike?

4.What was the highest return  reason for most customers?

5.What time of the year was products being returned the most?

**ANALYSIS AND INSIGHTS**

• Returns majorly occured in April and December throughout the year.This could be traced to seasonal purchases that occurs at those periods therefore the business should properly plan towards those periods to avoid preventable loss.

• East region showed the highest return rate of 5.9% with fashion and Electronics as the major drivers.Also transit time for this region spikes at day 5 giving reasons to slow deliveries experienced and more product returns.

• Fashion generated the highest return at 8.3% followed by Electronics at 7.3%.Clothings not delivered as at when stated can cause customers to reject deliveries as well as specifications of electronics not fully captured can lead to  a return.

• ‘Slow delivery’ and ‘Wrong Items’ are two major reasons for product returns.This should be checkmated because customers proritize getting their goods right on time and accurately delivered.

**RECOMMENDATIONS**

• On slow deliveries by March and November each year renegotiation with couriers offering faster shipping on high value electric orders should be considered to avoid extending transit days beyond day 5.

• The customer service team should be briefed on the most reoccuring return reasons so they can proactively  intimate customers  at the point of sale through chat/calls/emails reasons being that this action is cost effective rather than the cost of processing a returned order.

• Having a meaningful customer base of 7901 clients,segmentation of customers into groups such as first-time buyers,returning and high value customers will significantly improve customer retention and loyalty which inturn boost revenue.

• An audit of the product pages as regards images,specifications,size guides,product descriptions needs to be carried out prior to peak seasons to ensure every customer receive exactly what was being ordered from the page.

**SQL ANALYSIS**-

https://1drv.ms/w/c/15AA0654934D2775/IQDR-iuUG6gAQLJ9Okq895e4AR2bq6bZRWtVnIdA9V9z-QY?e=ttqEQw

QUERIES

CREATE TABLE sales(

order_id VARCHAR(15)NOT NULL,

customer_id VARCHAR(15) NOT NULL,

product_id VARCHAR(15) NOT NULL,

category VARCHAR(25) NOT NULL,

price DECIMAL(5,2),

discount DECIMAL(5,2),

quantity INTEGER,

payment_method VARCHAR(50)NOT NULL,

order_date DATE,

delivered_date DATE,

region VARCHAR(20)NOT NULL,

returned VARCHAR(20)NOT NULL,

request_date DATE,

return_reason VARCHAR(25)NOT NULL,

total_amount DECIMAL(5,2),

shipping_cost DECIMAL(5,2),

profit_margin DECIMAL(5,2),

customer_age INTEGER,

customer_gender VARCHAR (20));

CREATE TABLE sales_new(

order_id VARCHAR(15)NOT NULL,

customer_id VARCHAR(15) NOT NULL,

product_id VARCHAR(15) NOT NULL,

category VARCHAR(25) NOT NULL,

price DECIMAL(5,2),

discount DECIMAL(5,2),

quantity INTEGER,

payment_method VARCHAR(50)NOT NULL,

order_date DATE,

delivered_date DATE,

region VARCHAR(20)NOT NULL,

returned VARCHAR(20)NOT NULL,

request_date VARCHAR(20) NOT NULL,

return_reason VARCHAR(25)NOT NULL,

total_amount DECIMAL(10,3),

shipping_cost DECIMAL(5,2),

profit_margin DECIMAL(5,2),

customer_age INTEGER,

customer_gender VARCHAR (20));

ALTER TABLE sales_new ALTER COLUMN price TYPE NUMERIC(10, 2);

SELECT * FROM sales_new;

SELECT SUM (price * quantity )AS total_cost

FROM sales_new;



SELECT SUM(total_amount)AS total_sales

FROM sales_new;

SELECT COUNT(DISTINCT customer_id)AS total_customers

FROM sales_new;

SELECT SUM(quantity)AS total_quantity

FROM sales_new;

SELECT COUNT(DISTINCT order_id)AS total_orders

FROM sales_new;

SELECT  

 ROUND( 

 SUM(CASE WHEN returned = 'Yes' THEN quantity ELSE 0 END) * 100.0 /

 NULLIF(SUM(CASE WHEN Quantity > 0 THEN quantity ELSE 0 END), 0),2 )AS ReturnRate_Percent 

 FROM sales_new;

SELECT category, SUM(total_amount) AS total_sales

FROM sales_new

GROUP BY category

ORDER BY total_sales DESC 

LIMIT 5;

SELECT region,SUM(total_amount)AS total_sales

FROM sales_new

GROUP BY region

ORDER BY total_sales DESC;

SELECT category,COUNT(returned)AS returned_count

FROM sales_new

WHERE returned ='Yes'

GROUP BY category

ORDER BY returned_count DESC

LIMIT 5;

SELECT customer_id,SUM(total_amount)AS total_sales

FROM sales_new

GROUP BY customer_id

ORDER BY total_sales DESC

LIMIT 10;

**DATA SOURCE**

The dataset used in this project was sourced from kaggle-https://www.kaggle.com/datasets/angellawl/e-commerce-dataset-order-and-return


Built by Chinwe Ibe

**CONNECT WITH ME**

**LINKEDIN**-www.linkedin.com/in/
chinwe-ibe-431b86102

**EMAIL**-chukwuekechinwe@yahoo.com







