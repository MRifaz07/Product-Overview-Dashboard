# 📊 Product Usage & Retention Dashboard

An interactive Power BI dashboard built to analyze user behavior, feature adoption, churn trends, and revenue insights for a SaaS-style product. Designed with a clean 3-page layout, dark theme, and advanced interactivity features such as slicers, tooltips, and navigation buttons.

## 🧠 Project Summary

This dashboard provides actionable insights for product and growth teams by tracking key performance indicators (KPIs) such as:
- **Daily Active Users (DAU)** and **Monthly Active Users (MAU)**
- **Churn Rate** and **Feature Adoption**
- **Net Revenue**, **Stickiness %**, and **Engagement Trends**

## 🌟 Key Insights

- 📉 Stickiness dropped after Q2 2024 → retention at risk  
- ⚠️ Feature Y frequently used before churn → may need usability improvement  
- 👴 Older age groups have high usage but lower LTV  
- 🔍 Users engaging with < 2 features showed high churn tendency

## 📄 Dashboard Structure

### 1️⃣ Product Overview  
- KPIs: Total Users, Active Users, Churned Users  
- Revenue trends & filters

### 2️⃣ User Behavior  
- DAU, MAU, Stickiness %  
- Trends filtered by region, time, and age group

### 3️⃣ Feature Usage  
- Feature popularity & churn correlation  
- Feature adoption rate by age segment

## 🧮 Sample DAX Measures

```DAX
-- Stickiness %
Stickiness % = DIVIDE([DAU], [MAU]) * 100

-- Net Revenue
Net Revenue = 
CALCULATE(
    SUM(Orders[amount]) - SUM(Orders[discount_applied]),
    Orders[is_successful] = 1
)
