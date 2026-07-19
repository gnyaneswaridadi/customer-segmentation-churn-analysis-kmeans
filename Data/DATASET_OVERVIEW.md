# 📊 Dataset Overview

The dataset (`ecommerce_customer_churn_dataset.csv`) contains **50,000 customer records** (49,910 after cleaning) from an e-commerce platform, with **25 columns** spanning demographics, engagement behavior, purchase history, value metrics, and a churn label.

---

## Demographics
| Column | Description |
|---|---|
| `Age` | Customer's age |
| `Gender` | Customer's gender |
| `Country` | Customer's country |
| `City` | Customer's city |
| `Signup_Quarter` | Quarter in which the customer signed up (Q1–Q4) |

## Engagement Behavior
| Column | Description |
|---|---|
| `Login_Frequency` | How often the customer logs in |
| `Session_Duration_Avg` | Average time spent per session |
| `Pages_Per_Session` | Average number of pages viewed per visit |
| `Email_Open_Rate` | Percentage of marketing emails opened |
| `Social_Media_Engagement_Score` | Engagement level with the brand's social media |
| `Mobile_App_Usage` | Level of mobile app usage |
| `Customer_Service_Calls` | Number of support calls made |
| `Product_Reviews_Written` | Number of reviews the customer has written |

## Purchase Behavior
| Column | Description |
|---|---|
| `Membership_Years` | How long the customer has held an account |
| `Total_Purchases` | Total number of purchases made |
| `Average_Order_Value` | Average amount spent per order |
| `Cart_Abandonment_Rate` | Percentage of carts started but not completed |
| `Wishlist_Items` | Number of items saved to wishlist |
| `Days_Since_Last_Purchase` | Recency — days since the last order |
| `Discount_Usage_Rate` | How often the customer uses discounts/coupons |
| `Returns_Rate` | Percentage of orders returned |
| `Payment_Method_Diversity` | Number of different payment methods used |

## Value & Outcome
| Column | Description |
|---|---|
| `Lifetime_Value` | Total estimated value of the customer to the business |
| `Credit_Balance` | Store credit or balance on the account |
| `Churned` | **Target variable** — 1 if the customer churned, 0 if retained |

---

## At a Glance
- **Total columns:** 25
- **Total customers analyzed:** 49,910 (post-cleaning)
- **Churn rate:** 28.91%
- **Average lifetime value:** $1,440.58
- **Average purchases per customer:** 13.13

---

This mix of behavioral, transactional, and demographic signals is what makes the dataset well-suited for both churn analysis (what predicts churn) and customer segmentation (grouping customers by shared behavior patterns) — the two objectives this project addresses.
