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



3. What are the 3 top performing product categories in terms of how many `eCommerce_option="Payment"` sessions occured? *Use the categories table to get the category groups, NOT v2ProductCategory.*


the_count	|category
----|----
38642|	Apparel
27610	|Nest-USA
27610	|Home/Nest/


4. How many pageviews were for which denominations of gift cards? Assume that `v2ProductName` should contain "Gift Card" and sessions with type="PAGE" should be counted. Note that more than one pageview can happen per session so you will need to *add them up*, not just *count the records*.

v2ProductName	| f0_ 
--|--
Gift Card- $100.00|	104328
Gift Card - $250.00|	222128
Gift Card - $50.00	|100275
Gift Card - $25.00|	153649
