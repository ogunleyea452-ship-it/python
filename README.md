# RFM ANALYSIS (A CUSTOMER SEGMENTATION ANALYSIS IN RETAIL MARKETING)

## TABLE OF CONTENT
RFM ANALYSIS OVERVIEW

LANDING PAGE

DATA SOURCE

PYTHON LIBRARY USED

TOOL

TYPE OF ANALYSIS: BEHAVIORAL MODEL

DATA CLEANING & ETL

EXPLORATORY DATA ANALYSIS & PRE-PROCESSING

DATA ANALYSIS

AASSIGNING RANKS TO  RFM VALUES, MERGING ALLl DATAFRAMES AND  BUCKETING

INSIGHTS

RECOMMENDATIONS


## RFM ANALYSIS OVERVIEW
**RFM segmentation is a data-driven analysis grounded in behavioral economics, probability theory, and customer lifetime value modeling. It studies customers pruchase behavior then classifies the customers based on those behavioral patterns. RFM analyzes three key dimensions: 
**Recency (how recently they bought)** 
**Frequency (how often they buy)**, and **Monetary value (how much they spend)**. By scoring customers on each factor, we can instantly spot our best customers, identify those at risk of churning, and find hidden growth levers**


## LANDING PAGE
THE DATA-SET CONSISTS OF 8 COLUMNS:
![alt text](/columns.jpg)

## DATA SOURCE
[My link here](https://www.kaggle.com/datasets/ineubytes/online-retail-ecommerce-dataset/)


## PYTHON LIBRARY USED
- Pandas
- Matplotlib
- Seaborn 

## TOOL USED
Jupypter notebook; a web based Integrated Development Environment (IDE)

## TYPE OF ANALYSIS CARRIED OUT IN THIS PROJECT
- DESCRIPTIVE ANALYTICS

We examined the consumer purchase behavior based on;
- RECENCY OF PURCHASE
- FREQUENCY OF PURCHASE
- AVERAGE MONETARY VALUE PER INVOICE




## DATA CLEANING & ETL
- Null values were filled with the mode for object values and mean for continous values.
- Duplicates values were removed
- The revenue column was calculated by multiplying quantity and price then added to dataframe.
- Due to the data containing records from so many counteries, just **UNITED KINGDOM** transactions was filtered and analyzed.
![alt text](/cleaning.jpg)


## EXPLORATORY DATA ANALYSIS
![alt text](/EDA_Descriptive.jpg)
![alt text](/histogram.jpg)
![alt text](/boxplot.jpg)
![alt text](/outlieer_removal.jpg)

- The descriptive analysis image (first image) revealed the presence of outlier in the sold quantity column.The assertion was further confirmed in the 2nd and 3rd images of right skewed histplot and boxplotshowing the upper and lower data range.
- The last image showed the Inter-quantile range calculation and removel of the outlier to get evenly skewed data.



## DATA ANALYSIS

                     **RECENCY**
Recency: It measures (in days) how long it has been since a customer last made a purchase.
- Assumption: The more recently a customer purchased, the more likely they are to purchase again.

**Descriptive analysis of the Recency value**
![alt text](/image1.jpg)

In the above image:
For the UK retailer data, 
- 25% of the customers have a 25 day recency value. 
- 50% had a recency of 98 days.

**Insight**: This data reveals that the customers purchase health is really poor and this signals a churn risk.

             **FREQUENCY**
 Frequency: It measures the number of distinct purchase events in the analysis window. Analysis window should be at least 12 months.

 **Descriptive analysis of the Frequency value**  
 ![alt text](/image2.png)  

 - For a data collected within 24 months window, 18 days frequency value among 25% of the customers and 46 days frequency among 50% of its customers is really poor.

Insight: The frequency analysis reveals the poor state of customers purchase pattern and lack of repeated purchases from same customers,signals a churn tendencies.     

           **MONEYTARY VALUE**
 Monetary values(spend): Measures the average amount of money a customer had spent over a defined period. 

 **Descriptive analysis of Monetary values**
 ![alt text](/image3.png)   

 The image above gave the following revelations;
- 25% of the total customers spent an avearge on 134.30 British pounds per invoice of order
- 50%- of the total customers spent 206.66 British pounds per invoice of order
75%- 305.57 British pounds per invoice of order.

Insight: Even though these customers showed signs of low recency and frequency, they are heavy spenders.

## Assigning ranks to the RFM values, merging the all dataframes and bucketing.
- The RFM values were resize to percentile to achieve uniform number range then divided into buckets and labelled.
![alt text](/merge.jpg)
![alt text](/image4.jpg)
![alt text](/image5.jpg)


- Finally the customer category was counted and visualized with matplotlib.

##  Insights for Executive, Business Implication and Recommendation.

The RFM analysis conducted on the UK retailer dataset reveals significant patterns in customer purchasing behaviour over the observed two-year window. These insights highlight both opportunities and risks within the customer base and point toward actions required to improve customer retention and revenue performance.

🔵 1. Recency Analysis showed Strong Indication of Customer Churn

**Key Findings**

- 25% of total customers have not purchased in the last 25 days.

- The median customer (50th percentile) has a recency of 98 days, meaning half of the customer base has not made a purchase in over three months.

**Executive Insight**
This indicates a weak customer engagement cycle.

A recency spread this wide suggests that the company is losing active customers quickly.

The pattern strongly indicates a churn risk, with a large portion of the customer base no longer engaging regularly.

**Business Implication**

Without targeted re-activation efforts, the business will experience declining repeat sales, increased acquisition costs, and reduced customer lifetime value.

🟠 2. Frequency Analysis — Low Repeat Purchase Rates

Key Findings

25% of total customers purchased only once every 18 days.

The median (50%) purchased once every 46 days.

**Executive Insight**

These frequency values are low for a two-year analysis window and clearly reflect weak repeat-purchase behavior.

Customers do not exhibit habitual buying patterns, implying that the brand is not embedded into their regular consumption cycle.

**Business Implication**

- Low purchase frequency signals:

Insufficient customer loyalty

High dependency on single-transaction shoppers

Limited effectiveness of retention and cross-sell programs

This further strengthens the evidence of churn tendencies, as customers are not returning frequently enough to sustain long-term revenue growth.

🟢 3. Monetary Value Analysis — Customers Who Do Spend, Spend Well

Key Findings

- The bottom quartile (25%) spend £134 per average invoice.

- The median customer spends £206 per invoice.

- The top quartile (75%) spend over £306 per invoice.

**Executive Insight**

Despite low recency and frequency, the monetary value is relatively strong, indicating:

When customers do purchase, they spend significantly.

There exists a segment of high-value customers who contribute disproportionately to revenue.

**Business Implication**

High spend per order provides an opportunity to:

Strengthen loyalty among top spenders.

Reduce churn impact by nurturing these high-value clients.

Design targeted promotions to improve purchase frequency while protecting revenue.


## Executive Recommendations

1. Launch an aggressive re-engagement strategy which will target customers with recency above 60–90 days.

Use personalized email campaigns, discounts, and win-back incentives.

2. Strengthen loyalty and retention programs

Introduce tier-based rewards for high spenders.

Build subscription or auto-replenishment programs where possible.

3. Increase purchase frequency

Cross-sell and upsell campaigns triggered after each purchase.

Time-based nudges such as “It’s been X days since your last order.”

4. Protect the top 20% of customers

VIP benefits, early product access, premium customer service.

Avoid churn of the high-value segment that drives a major share of revenue.

















