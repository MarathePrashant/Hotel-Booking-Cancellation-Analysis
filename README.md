# 🏨 Hotel Booking Cancellation Analysis & Revenue Recovery

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-CC292B?style=for-the-badge&logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

> **Business Objective:** Diagnose cancellation drivers across 118,000+ booking records to mitigate a 37.14% cancellation rate representing an estimated $25.91M in revenue exposure.

---

## 📌 Executive Summary
High cancellation rates destabilize hotel operations, lead to suboptimal room pricing, and cause substantial unrecoverable revenue loss. This project investigates booking records from both City and Resort hotels over a multi-year window. 

By combining **Python (Pandas, Seaborn)** for exploratory data cleaning and statistical analysis, **SQL** for relational metric aggregations, and **Power BI (DAX)** for interactive reporting, this analysis identifies the key drivers of cancellations and provides actionable pricing and operational strategies for hotel leadership.

---

## 📊 Interactive Dashboard Preview

*(Add a screenshot of your Power BI dashboard here. You can drag and drop an image directly into GitHub's editor)*

> **Interactive Report:** *(Optional: Insert link to Power BI Service / NovyPro live report if published)*

---

## 🎯 Key Business Metrics & KPIs Analyzed

| Metric | Recorded Value | Business Implication |
| :--- | :--- | :--- |
| **Total Analyzed Records** | 118,000+ | Large-scale sample across City & Resort hotels |
| **Overall Cancellation Rate** | **37.14%** | More than 1 in 3 bookings failed to materialize |
| **Estimated Revenue Loss** | **~$25.91M** | Total pipeline value lost due to cancellations |
| **Average Daily Rate (ADR)** | Analyzed by Segment | Dynamic pricing fluctuations impact booking stability |
| **Lead Time Threshold** | Critical inflection at >60 days | Longer lead times correlated with steep cancellation increases |

---

## 🔍 Key Findings & Root Cause Analysis

1. **Lead Time Correlation:** 
   - Bookings made **60+ days in advance** exhibited significantly higher cancellation rates compared to short-notice bookings (<14 days), as traveler schedules remain fluid without upfront financial commitment.
2. **Deposit Policy Anomalies:** 
   - Analysis revealed counter-intuitive patterns where specific distribution channels with non-refundable deposits had elevated cancellations, primarily tied to bulk corporate or intermediary agency blocks rather than direct individual guests.
3. **Distribution Channel Vulnerability:** 
   - Online Travel Agencies (OTAs) accounted for the largest volume of gross bookings but also exhibited the highest cancellation churn relative to direct hotel website bookings.
4. **Repeated Guest Loyalty:** 
   - Repeat visitors had a cancellation rate below 15%, proving that direct customer relationship management strongly protects booked revenue.

---

## 💡 Strategic Recommendations for Management

* **Dynamic Overbooking Thresholds:** Implement dynamic overbooking limits tied to lead time and season—allowing higher buffer capacity during peak OTA reservation windows to maintain target occupancy.
* **Tiered Non-Refundable Discounts:** Offer a small targeted rate discount (e.g., 5–8% off ADR) for guests who select a non-refundable rate upfront for bookings made >45 days in advance.
* **Pre-Arrival Engagement Automation:** Deploy automated confirmation touchpoints at 30 days, 14 days, and 3 days prior to arrival for high-lead-time reservations to encourage itinerary confirmation or early release.
* **Incentivize Direct Bookings:** Promote direct-booking loyalty perks (complimentary breakfast, free room upgrade eligibility) to shift volume away from high-churn OTA channels toward direct channels.

---

## 🛠️ Tech Stack & Workflow

```text
├── Data Extraction & Cleaning  --> Python (Pandas, NumPy)
│                                 - Handled missing values (children, agent, company)
│                                 - Removed undefined meal/distribution categories
│                                 - Created engineered features (lead time bins, total stay duration)
│
├── Relational Querying         --> SQL (Aggregations, CTEs, Window Functions)
│                                 - Segmented cancellation ratios across hotel types and seasons
│
└── Business Intelligence       --> Power BI
                                  - Star Schema Data Modeling
                                  - Custom DAX Measures (Cancellation Rate %, Revenue Loss, ADR Variance)
                                  - Dynamic Filter Slicers by Market Segment, Deposit Type & Date
