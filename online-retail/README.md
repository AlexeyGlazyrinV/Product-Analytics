# MAU, APRU & Loyalty Funnel: Online Retail

## Business context
A product/growth team wants to understand how the active customer base and revenue per user evolve over time, and which customer segments drive revenue - to prioritize retention spend correctly

## Question
How do MAU and ARPU trend month over month, and which purchase-frequency segments contribute most to revenue?

## Data
~ 1M transactions from a UK online gift retailer, Dec 2009 - Dec 2011 (805K after cleaning).
Fields:
- Invoice
- StockCode
- Quantity
- InvoiceDate
- Price
- CustomerID
- Country
Source: [Kaggle - Online Retail II (UCI)] (https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)

## Method
- MAU / ARPU computed monthly
- Customer segmentation by purchase frequency
- Cohort retention analysis by first-purchase month

## Result
- 45% customers generate 87.7% of total revenue
- Retention drops from 100% to 21% within the first month post-purchase, then stabilizes
- A December 2010 ARPU spike was diagnosed as a broad shift toward higher order values, not handfulof outlier orders - verified by decomposing ARPU and testing the outlier-order hypothesis directly, rather than assumed at first glance

## Recommendation
Focus retention mechanics on the first month of the customer lifecycle, where most future-loyal customers are lost, rather than spreading budget evenly across the base
