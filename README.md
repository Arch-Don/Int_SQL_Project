# SQL - Sales Analysis
## Overview
Analysis of customer behavior, retention, and lifetime value for an e-commerce company to improve customer retention and maximize. revenue 
## Business Question
1. **Customer Segmentation:** Who are our most valued customers?
2. **Cohort Analysis:** How do different customer groups generate revenue?
3.  **Retention Analysis:** Who has not purchased recently
## Analysis Approach
### 1. Customer Segmentation Analysis
- Categorized customer based on Life Time Value (LTV)
- Assigned customer to High, Mid and Low-value segmentation
- Calculated key metrics: total revenue
### 💻Query: [1_customer_segmentation.sql](/1_customer_segmtation.sql)
### visualization📊:
*Customer Segmentation Table*
![Customer Segmentation Table](/images/1_sql1.png)
*Customer Segmentation Graph*
![Customer Segmentation Graph](/images/1_sql2.png)
**🗝Key Findings:**
- High-value segment drives 66% of revenue($135.4M)
- Mid-value segment drives 32% of revenue($66.6M)
- Low-value segment accounts for 2% of revenue($4.3M)
## 💡Business Insights:
- High-value: Offer premium membership programme as losing one customer significantly impacts revenue
- Mid-value: Personalize Promotions, with potential $66.6M➡$135.4M revenue opportunity
- Low-value: Design re-engagement campaigns and price-sensitive promotions to increase purchase frequency

### 2. Cohort Analysis
- Track Revenue and Customer count per cohort
- Cohorts where grouped by year of first purchase
- Analyzed customer  retention at a cohort level
### 💻Query: [2_cohort_analysis.sql](/2_cohort_analysis.sql)
### visualization📊:
*Cohort Analysis Table*
![Cohort Analysis](/images/sql2.png)
*Cohort Analysis Graph*
![Cohort Analysis](/images/sql2_img.png)
**🗝Key Findings:**
- Revenue per customer decreases over time
    - 2022-2024 performance are worst compared to earlier cohorts
    - NOTE: Increasing net revenue is due to a large customer base not customer value 
## 💡Business Insights:
- Value extracted from customers is decreasing over time and needs investigation
- In 2023 we saw a drop in number of customers, which is concerning
- With both reducing LTV and customer acquisition, the company is facing a potential revenue decline

### 3. Customer Retention
- Identified customers at risk of churning
- Analyzed last purchase patterns
- Calculated customer-specific metrics
### 💻Query: [3_retention_analysis.sql](/3_retention_analysis.sql)
### visualization📊:
![Customer Retention](/images/3_sql1.png)
**🗝Key Findings:**
- Cohort churn stabilizes at ~90% after 2-3 years, indicating a predictable long-term retention pattern
- Retention rates are consistently low across all cohorts
- Newer cohorts show similar trajectories, signaling that without intervention, future cohorts will follow the same pattern 
## 💡Business Insights:
- Strengthen early engagement strategies to target first 1-2 years with onboarding incentives loyalty rewards, and personalized offers to improve long term retention.
- Re-engage high-value churned customers by focusing on targeted win-backs campaigns rather than broad retention efforts, as reactivating valuable users may yield higher ROI.
- Predict and preempt churn risk using customer-specific indicators 

## Technical Details
- **Database:** PostgreSQl
- **Analysis Tools:** PostgreSQL
- **Virtualization:** ChatGPT and PostgreSQL