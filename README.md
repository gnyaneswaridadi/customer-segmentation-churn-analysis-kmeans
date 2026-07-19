# E-Commerce Customer Churn Analysis & Segmentation

## Overview
This project analyzes an e-commerce customer dataset to understand churn behavior and segments customers into actionable groups using K-Means clustering. The goal is to identify which types of customers are most likely to churn and suggest where retention efforts should focus.

## Dataset
`ecommerce_customer_churn_dataset.csv` — contains customer demographics (Age, Gender, Country, City), engagement metrics (Login_Frequency, Session_Duration_Avg, Email_Open_Rate, Social_Media_Engagement_Score), purchase behavior (Total_Purchases, Cart_Abandonment_Rate, Lifetime_Value), and a binary `Churned` label.

> **Note:** Place the CSV in a `data/` folder in the repo root (or update the file path in the notebook to match wherever you keep it) before running.

## Approach
1. **Data Cleaning** — handled missing values (median imputation, excluding the target column), removed duplicate rows, and filtered out-of-range values (e.g. invalid ages, negative purchase counts).
2. **Exploratory Data Analysis** — churn rate, lifetime value distribution, purchase frequency, and engagement patterns split by churn status.
3. **Feature Engineering** — combined related raw signals into composite `Activity_Score` and `Engagement_Score` features.
4. **K-Means Clustering** — scaled features with `StandardScaler`, chose cluster count via the Elbow Method, and validated cluster quality with a Silhouette Score.
5. **Segment Profiling** — clusters are ranked and labeled programmatically based on their actual behavioral averages (not hardcoded index-to-name mapping), producing five segments: Loyal Customers, Regular Customers, Discount Seekers, Window Shoppers, and Inactive Customers.
6. **Business Insight** — churn rate compared across segments to identify which groups need retention attention.

## Key Findings
- **Silhouette Score: ~0.18** — indicates moderate cluster overlap. Customer behavior in this dataset trends more continuous than sharply segmented, so these groups are best read as directional tendencies rather than hard categories.
- **Inactive Customers** and **Window Shoppers** show the highest churn rates.
- **Loyal Customers** and **Regular Customers** churn the least and represent the base most worth protecting.

## Tools Used
- Python (pandas, numpy)
- matplotlib, seaborn (visualization)
- scikit-learn (StandardScaler, KMeans, silhouette_score)

## How to Run
1. Clone this repo.
2. Install dependencies: `pip install -r requirements.txt`
3. Place `ecommerce_customer_churn_dataset.csv` in a `data/` folder (or adjust the path in the notebook).
4. Open `ecommerce_churn_kmeans_analysis.ipynb` in Jupyter or Colab and run all cells.

## Possible Next Steps
- Train a supervised model (logistic regression / random forest) to predict churn directly and rank feature importance.
- Test alternate values of *k* against the silhouette score to see if a different cluster count separates segments more cleanly.

## Key Business Insights

- Highly engaged customers are less likely to churn.
- Customers with frequent purchases generate higher lifetime value.
- Cart abandonment is strongly associated with window-shopping behavior.
- Discount dependency affects long-term customer loyalty.
- Inactive customers represent the highest churn-risk group.

## Results

The K-Means clustering model successfully identified five meaningful customer segments:

1. Loyal Customers
2. Regular Customers
3. Window Shoppers
4. Discount Seekers
5. Inactive Customers

These segments provide actionable insights for:

- Customer Retention
- Personalized Marketing
- Revenue Optimization
- Customer Relationship Management
- Strategic Decision-Making

---

## Future Improvements

- Apply advanced clustering techniques (DBSCAN, Hierarchical Clustering)
- Build churn prediction models
- Develop interactive dashboards using Power BI or Tableau
- Deploy the model as a web application

## Conclusion

This project demonstrates how customer analytics and machine learning can be combined to identify meaningful customer segments and uncover business insights. Through behavioral analysis, feature engineering, and K-Means clustering, the project provides a data-driven approach to understanding customer behavior and improving business decision-making.

---

## Author

**Gnyaneswari Dadi**

Aspiring Data Analyst | Business Analytics Enthusiast | Machine Learning Learner
