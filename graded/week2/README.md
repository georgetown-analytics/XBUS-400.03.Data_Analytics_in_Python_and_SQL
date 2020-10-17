# Module 3 Week 2 Graded Lab directions

### Setup

1. Add the `data-to-insights` project to your BigQuery project (https://console.cloud.google.com/bigquery?p=data-to-insights&page=ecommerce)

2. Submit SQL statements that answer each of the following questions. You will need to use the `all_sessions`, `categories`, and `products` tables.

### Questions

1. Determine the total views per referring site by counting `product_views` per `channelGrouping`.


unique_visitors	|channelGrouping
---|---
38101|	Social
57308|	Referral
11865|	Paid Search
211993|	Organic Search
3067	|Display
75688	|Direct
5966	|Affiliates
62	|(Other)


2. What are the 3 top performing product categories in terms of how many `eCommerce_option="Payment"` sessions occured?


the_count	|category
----|----
38642|	Apparel
27610	|Nest-USA
27610	|Home/Nest/


3. How many pageviews were for which denominations of gift cards? Assume that `v2ProductName` should contain "Gift Card" and sessions with type="PAGE" should be counted. Note that more than one pageview can happen per session!


v2ProductName	| f0_ 
--|--
Gift Card- $100.00|	104328
Gift Card - $250.00|	222128
Gift Card - $50.00	|100275
Gift Card - $25.00|	153649


4. What 5 products have the largest restocking lead time?


name|	restockingLeadTime
---|---
 Cam Indoor Security Camera - USA	|42
 Stylus Pen w/ LED Light|	39
Recycled Mouse Pad|	39
Leatherette Journal|	36
Gunmetal Roller Ball Pen|	36

