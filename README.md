# CUSTOMER-LIFETIME-VALUE

# Cohort Analysis and CLV Prediction

## Overview

This project aims to improve the calculation of Customer Lifetime Value (CLV) by using cohort analysis, as opposed to relying solely on a simplistic method based on purchase events. The new approach considers all users who visited the site, using their first visit as a proxy for registration. Furthermore, the analysis predicts future revenue for newly acquired user cohorts, providing a more comprehensive view of expected lifetime value.

## Task Breakdown

### Objective

- Calculate weekly average revenue per user for each registration cohort.
- Calculate cumulative revenue for each cohort over time.
- Predict future revenue for new user cohorts based on historical data.
- Visualize the results using Google Sheets with conditional formatting to highlight key trends.

### Key Points

- **Week Cohorts:** Cohorts are based on the week of the first visit, which is treated as the registration date.
- **Revenue Calculation:** Revenue per user is calculated for each cohort and expressed as an average for each week since registration.
- **Cumulative Revenue:** Cumulative revenue is calculated by adding each week's revenue to the previous week's total, showing how the cohort's revenue grows over time.
- **Revenue Prediction:** Future revenue for new cohorts is predicted for the next 12 weeks using the average growth rates of previous cohorts.

### Steps

1. **Data Extraction and Weekly Revenue by Cohorts**
   - Data is pulled from the `turing_data_analytics.raw_events` table, where the first visit event marks the registration date.
   - Weekly revenue is calculated and divided by the number of users in each cohort to determine the average revenue per user.
   
2. **Cumulative Revenue Calculation**
   - Revenue is accumulated over time, tracking the growth in revenue for each cohort as they progress through the weeks since their registration.

3. **Revenue Prediction for Future Cohorts**
   - Using the cumulative growth percentages derived from historical cohorts, future revenue for new cohorts is predicted for the next 12 weeks.

4. **Visualization in Google Sheets**
   - The calculated data is transferred to Google Sheets for visualization, where conditional formatting is applied to highlight significant trends in the data.
   
5. **Final Output**
   - The final visualizations provide both a historical overview and future revenue predictions for the various user cohorts, offering insights into customer lifetime value.

## Visualizations

The visualizations were created in **Google Sheets**, displaying the following:

1. **Weekly Average Revenue by Cohorts (USD)**
2. **Cumulative Revenue by Cohorts (USD)**
3. **Revenue Prediction by Cohorts (USD)**

Each of these tables includes conditional formatting, making it easy to identify important trends, including revenue growth, plateauing, or decline over time.

## Evaluation Criteria

The project will be evaluated on:

- Correct identification of necessary data columns and metrics.
- Accurate calculation of weekly revenue, user counts by cohorts, and cumulative revenue.
- Google Sheets visualization with at least 3 tables, including conditional formatting.
- Clear analysis of trends and identification of key insights.

## Sample Questions

1. **Does including all customers (not only the ones who purchased something) influence the calculation of CLV?**
2. **Is your previously calculated CLV (using Shopify’s formula) still accurate?**
3. **How does cohort analysis help you understand future revenue?**
4. **If we knew that our business Take Rate (percentage of revenue treated as profit) is only 10%, would this change our estimation of CLV?**
5. **What potential limitations or caveats might arise from using cohort analysis in this context?**
