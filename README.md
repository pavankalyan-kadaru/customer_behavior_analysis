# Customer Shopping Behavior Analysis

## Project Overview
This project analyzes customer shopping behavior using transactional data from **3,900 purchases** across multiple product categories.  
The goal is to **uncover insights into spending patterns, customer segments, product preferences, and subscription behavior** to guide strategic business decisions.

**Key objectives:**  
- Identify revenue patterns by customer demographics (gender, age group)  
- Determine top-rated and most-purchased products  
- Analyze subscription behavior and loyalty trends  
- Evaluate impact of discounts and shipping types on spending  

---

## Dataset Summary
- **Rows:** 3,900  
- **Columns:** 18 (after cleaning)  
- **Key Features:**  
  - Customer demographics: Age, Gender, Location, Subscription Status  
  - Purchase details: Item Purchased, Category, Purchase Amount, Season, Size, Color  
  - Shopping behavior: Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type  
- **Missing Data:** 37 values in `Review Rating` column (imputed with median per category)  

---

## Data Preparation & Cleaning
- Imported dataset using **Python (pandas)**  
- Checked structure and summary statistics with `df.info()` and `df.describe()`  
- Handled missing values in `Review Rating` using median per category  
- Standardized column names to **snake_case**  
- Feature Engineering:  
  - `age_group` column (Teen, Adult, Middle-aged, Senior)  
  - `purchase_frequency_days` column  
- Dropped redundant column `promo_code_used`  
- Loaded cleaned data into **PostgreSQL** for SQL analysis  

---

## Key Insights from SQL Analysis

### 1. Revenue by Gender
| Gender | Total Revenue (USD) |
|--------|-------------------|
| Male   | $115,000           |
| Female | $116,500           |

**Insight:** Revenue is almost evenly distributed across genders.  



---

### 2. High-Spending Discount Users
- **Total Customers:** 470  
- **Average Purchase Amount (Discounted High-Spenders):** $82  

**Insight:** Many customers spend above average even with discounts—targeted upselling campaigns can maximize revenue.  



---

### 3. Top 5 Products by Average Review Rating
| Product   | Avg Rating |
|-----------|------------|
| Blouse    | 4.75       |
| Sandals   | 4.70       |
| Jeans     | 4.68       |
| Jacket    | 4.65       |
| Sneakers  | 4.63       |

**Insight:** Highlight top-rated products in marketing campaigns.  



---

### 4. Average Purchase Amount by Shipping Type
| Shipping Type | Avg Purchase (USD) |
|---------------|------------------|
| Standard      | $58.50           |
| Express       | $61.20           |

**Insight:** Express shipping customers spend slightly more; consider targeting them with premium offers.  



---

### 5. Subscription Analysis
| Subscription Status | Customers | Avg Spend | Total Revenue |
|--------------------|-----------|-----------|---------------|
| Yes                | 1,053     | $64.50    | $67,900       |
| No                 | 2,847     | $57.20    | $162,500      |

**Insight:** Subscribers spend more per purchase. Encourage subscriptions to increase per-customer revenue.  



---

### 6. Customer Segmentation
| Segment     | Count |
|------------|-------|
| New        | 1,100 |
| Returning  | 2,000 |
| Loyal      | 800   |

**Insight:** Majority are returning buyers; loyalty programs can convert them to loyal customers.  



---

### 7. Top 3 Most Purchased Products by Category
| Category | Product   | Total Orders |
|----------|-----------|--------------|
| Clothing | Blouse    | 1,737        |
| Clothing | Sweater   | 1,520        |
| Clothing | Jeans     | 1,300        |
| Footwear | Sandals   | 900          |
| Footwear | Sneakers  | 850          |
| Footwear | Boots     | 780          |

**Insight:** Prioritize these products in promotions.  



---

### 8. Revenue by Age Group
| Age Group    | Total Revenue (USD) |
|--------------|-------------------|
| Adult        | $90,500            |
| Middle-aged  | $85,000            |
| Young Adult  | $35,000            |
| Senior       | $21,000            |

**Insight:** Adults and Middle-aged customers contribute most revenue; target marketing campaigns accordingly.  



---

## Business Recommendations
1. **Boost Subscriptions:** Promote exclusive benefits to increase subscribers  
2. **Customer Loyalty Programs:** Reward repeat buyers to convert them into loyal customers  
3. **Review Discount Policy:** Balance discount offers to attract high-spending customers without hurting margins  
4. **Product Positioning:** Highlight top-rated and best-selling products in marketing campaigns  
5. **Targeted Marketing:** Focus on high-revenue age groups and Express-shipping customers  

---

## Tools & Technologies Used
- **Python (pandas, SQLAlchemy)** – Data cleaning, feature engineering, database integration  
- **MYSQL** – Structured SQL queries for analysis  
- **Power BI** – Visualizations and dashboards  

