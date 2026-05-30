# Profit-Optimized Customer Retention System
I am changing this a bit 
## Overview

This project extends a traditional churn prediction task into a **profit-driven retention decision system**. Instead of only identifying customers likely to churn, the goal is to determine **which customers should be targeted with retention offers in order to maximize expected business value**.

The system combines calibrated churn probabilities, customer value estimation, and campaign cost assumptions to compute the **expected financial impact of targeting each customer**. Customers are then prioritized based on their economic value rather than churn probability alone.



## Connection to the Churn Classification Project

This project builds directly on the **Customer Churn Classification** project.

- The **churn classification project** focused on training machine learning models to predict the probability of customer churn.
- This project uses those predicted probabilities to design a **cost-sensitive retention strategy**.

Together, the two projects demonstrate the full workflow of applying machine learning in a business setting:

1. **Predict churn probability** using classification models.
2. **Use those probabilities to optimize retention decisions** and maximize profitability.



## Method

The system follows these steps:

1. **Predict churn probability** using a calibrated Random Forest model.
2. **Estimate Customer Lifetime Value (CLV)** using a simple proxy based on monthly charges.
3. **Define campaign assumptions**, including retention offer cost and success rate.
4. **Compute expected value for each customer**: Expected Value = P(churn) × CLV × success_rate − retention_cost


5. **Rank customers by expected value** and target the most profitable ones.

Two targeting strategies were evaluated:
- **Budget-constrained targeting** using expected value ranking.
- **Probability threshold targeting** using an optimal churn probability cutoff.


## Key Insight

The analysis shows that **only a small fraction of customers are economically worth targeting**. By focusing retention efforts on high-value churn risks, the system enables organizations to allocate retention budgets more efficiently and generate measurable profit.



## Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
