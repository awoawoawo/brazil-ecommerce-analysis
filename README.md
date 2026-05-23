## Business Overview

This project analyzes a Brazilian e-commerce dataset consisting of approximately **100,000 orders** and **over 90,000 customers**, generating total sales revenue exceeding **R$18 million**. The dataset captures multiple dimensions of the business, including transactional data, product categories, payment values, and customer geographic information.

An in-depth analysis was conducted to evaluate brazil ecommerce dataset performance over the observed period (2016–2018).

This analysis aims to provide actionable insights that can support business decision-making, particularly in optimizing product strategy, improving revenue quality, and identifying high-performing markets. The findings are intended to help stakeholders better understand where the business is performing well and where there are opportunities for growth or improvement. 

The key insights and recommendations focus on the following areas:
- **Sales Trend Analysis** - focuses on how the business evolves over time by examining revenue, number of orders, and average order value (AOV).

- **Product Category Performance** - explores how different product categories contribute to the business. It highlights which categories drive revenue, which rely on high transaction volume, and which represent high-value but lower-frequency purchases.

- **Regional Performance Analysis** - focuses on revenue distribution across customer states. 

> All data processing and analysis were performed using Python (pandas, numpy). Visualization was created using matplotlib and seaborn.

## Data Dictionary

The dataset contains **111,015 rows**, structured at the **item level**, meaning each row represents a single product within an order. As a result, one `order_id` may appear multiple times depending on the number of items purchased in that order.

| Column Name                     | Description |
|--------------------------------|-------------|
| order_id                       | Unique identifier for each order. One order can contain multiple items. |
| order_status                   | Current status of the order (e.g., delivered, shipped, canceled). |
| order_purchase_timestamp       | Timestamp when the order was placed by the customer. |
| order_approved_at              | Timestamp when the payment for the order was approved. |
| order_delivered_carrier_date   | Timestamp when the order was handed over to the logistics carrier. |
| order_delivered_customer_date  | Timestamp when the order was delivered to the customer. |
| order_estimated_delivery_date  | Estimated delivery date provided at the time of purchase. |
| customer_id                    | Unique identifier for each customer order (can repeat for same customer). |
| customer_unique_id             | Unique identifier for each customer (consistent across multiple orders). |
| customer_city                  | City where the customer is located. |
| customer_state                 | State (region) where the customer is located. |
| customer_zip_code_prefix       | Prefix of the customer’s zip code. |
| order_item_id                  | Item sequence number within an order (indicates multiple items per order). |
| freight_value                  | Shipping cost paid for the item. |
| price_x                        | Price of the product item (excluding shipping). |
| product_category_name_english  | Product category in English. |
| product_id                     | Unique identifier for each product. |
| shipping_limit_date            | Deadline for the seller to ship the order. |
| delivery_time                  | Time taken from shipment to delivery. |
| delay_status                   | Indicator of whether the delivery was on time or delayed. |
| profit                         | Estimated profit from the order or item. |
| order_month                    | Month when the order was placed. |
| order_year                     | Year when the order was placed. |
| total_spending                 | Total amount spent by the customer for the order. |
| total_order                    | Total number of orders associated with the customer or transaction. |

## Insight Deep-Dive

## Sales Trend

- Total sales during 2017–2018 reached approximately **R$ 13.3 million**, with monthly sales ranging from around **R$ 118k to R$ 991k**.
- Sales experienced a significant spike in **November 2017**, reaching the highest level during the observed period.
- Following the November 2017 peak, sales declined sharply in **December 2017**, recovered in **January 2018**, and decreased again in **February 2018**.
- From March to May 2018, sales showed moderate growth and relative stability. However, beginning in **June 2018**, sales started to decline again and continued trending downward afterward.
- Most product categories followed a similar overall sales pattern, including a noticeable spike in **November 2017**.

## Product Category Performance

- The best-performing product category was Health Beauty, generating approximately **R$ 1.2 million** in total sales.
- The worst-performing category was Security and Services, contributing only around **R$ 283** in total sales, which may indicate incomplete or missing data.
- In **December 2017**, the decline in sales was primarily driven by:
  - Bed Bath Table
  - Health Beauty
  - Watches Gift
- In **February 2018**, the decline was mainly driven by:
  - Watches Gift
  - Bed Bath Table
- In **June 2018**, all major categories experienced another decline, with Watches Gift showing a significantly sharper drop compared to the others.
- In **August 2018**, Watches Gift continued to decline, while Bed Bath Table and Health Beauty experienced sales spikes during the same period.

## Regional Performance

- Sales trends across all states followed generally similar patterns over time.
- São Paulo (SP) was the dominant contributor to total sales and acted as the primary driver of overall regional sales performance.
    
## Recommendations

Based on the uncovered insights, here are actionable steps to improve business performance:

## Sales Trend

- Prepare targeted recovery campaigns immediately after major sales spikes, especially following November peak periods, to reduce the sharp decline typically occurring in December and February.
- Maintain stable inventory and promotional activity for key product categories such as Watches Gift, Bed Bath Table, and Health Beauty, as these categories were the primary contributors to several sales declines.
- Closely monitor the Watches Gift category during periods of declining sales, particularly in February, June, and August 2018, and consider implementing category-specific discounts, bundling strategies, or seasonal campaigns to stabilize performance.
- Replicate successful strategies from November 2017, including promotional timing and campaign intensity, while ensuring that demand remains sustainable in subsequent months.
- Develop seasonal sales planning based on recurring monthly patterns to better anticipate periods of decline and proactively mitigate revenue drops.

## Product Category Performance

- Prioritize high-performing categories such as Health Beauty through expanded product offerings, targeted promotions, and optimized inventory management.
- Validate the Security and Services category data to determine whether the extremely low sales value was caused by missing or incomplete records.
- Closely monitor the Watches Gift category, as it consistently contributed to multiple sales declines across different time periods.
- Perform deeper analysis on Bed Bath Table and Watches Gift to identify factors contributing to recurring sales decreases, such as pricing, competition, or changing customer preferences.
- Apply category-specific marketing and promotional strategies instead of using uniform campaigns across all categories.

## Regional Performance

- Prioritize operational resources, marketing campaigns, and inventory allocation in São Paulo (SP), as it is the largest contributor to overall sales.
- Reduce dependency on SP by identifying growth opportunities and strengthening sales performance in lower-performing states.
- Conduct regional segmentation analysis to identify states with strong growth potential and develop more targeted regional strategies.
- Since sales trends are relatively consistent across states, nationwide campaigns may be effective when supported by localized adjustments and optimizations.
