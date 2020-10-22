# Module 3 Week 2 Graded Lab directions

### Setup

1. Add the `data-to-insights` project to your BigQuery project (https://console.cloud.google.com/bigquery?p=data-to-insights&page=ecommerce)

2. Submit SQL statements that answer each of the following questions. You will need to use the `all_sessions`, `categories`, and `products` tables. Use the "Preview" functionality to browse their schemas before starting to answer the questions.

### Questions

1. What 5 products have the largest restocking lead time?

name|	restockingLeadTime
---|---
 Cam Indoor Security Camera - USA	|42
 Stylus Pen w/ LED Light|	39
Recycled Mouse Pad|	39
Leatherette Journal|	36
Gunmetal Roller Ball Pen|	36


2. Determine the total views per referring site by aggregating `pageviews` per `channelGrouping`.


f0_ |	channelGrouping
--- | ---
15361488|	Social
113238990|	Referral
18569060|	Paid Search
179185663|	Organic Search
4168902	|Display
85731192|	Direct
2872532	|Affiliates
34789	|(Other)



3. What are the 3 top performing product categories? Consider a product to be high performing if it has many session records with the `eCommerceAction_option` column matching the value `"Payment"`. Connect the records in `all_sessions` to the `category` table based on the fact that `productSKU` is a foreign key between them to aggregate them by category. *Please do NOT use v2ProductCategory which is in the all_sessions table, we are working on JOINs!*


the_count	|category
----|----
38642|	Apparel
27610	|Nest-USA
27610	|Home/Nest/


4. How many `pageviews` were for which denominations of gift cards? Use the `all_sessions` table to find this out. Use the fact that `all_session.v2ProductName` contains the word "Gift Card" in it to limit your calculation agiainst records that are for Gift Card products. In addition, restrict your query to sessions where `all_session.type` exactly matches the string `"PAGE"`. Note that more than one pageview can happen per session so you will need to *add them up*, not just *count the resulting records*.

*Note: Because there is no ORDER BY, your answer might be in a different order, and that is ok!*

v2ProductName	| f0_ 
--|--
Gift Card- $100.00|	104328
Gift Card - $250.00|	222128
Gift Card - $50.00	|100275
Gift Card - $25.00|	153649
