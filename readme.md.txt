# Customer Segmentation using RFM & K-Means

## Business Problem

A mid-sized D2C retail brand was experiencing flat repeat purchase rates and rising marketing costs.  
Discounts were applied broadly, without understanding customer differences.

There was no structured customer segmentation strategy.

The objective of this project was to build a data-driven segmentation model to enable:
- Personalized marketing
- Improved retention
- Smarter discount allocation
- Better customer targeting


---

## Dataset

Online Retail transactional dataset (2010–2011)

After cleaning:
- 397,885 valid transactions
- 4,338 unique customers
- 1 year of purchase history

Data cleaning steps:
- Removed cancelled invoices
- Removed missing Customer IDs
- Removed negative quantities and prices
- Created OrderValue = Quantity × UnitPrice


---

## Methodology

### 1. RFM Feature Engineering

Each customer was aggregated into three behavioral metrics:

- **Recency** – Days since last purchase
- **Frequency** – Number of unique invoices
- **Monetary** – Total spend (log-transformed)

Monetary was log-transformed to reduce skewness and stabilize clustering.


### 2. Feature Scaling

StandardScaler was applied to ensure equal contribution of features, as K-Means relies on Euclidean distance.


### 3. Clustering

- Elbow Method used to determine optimal K
- Silhouette Score used for validation
- K = 4 selected for interpretability and strong separation

K-Means clustering was then applied to segment customers.


### 4. Visualization

- PCA used to project clusters into 2D space
- Segment size distribution visualized
- Average RFM values compared across segments


---

## Customer Segments Identified

### 1. VIP / Power Buyers
- Very recent purchases
- Extremely high frequency
- Highest spending customers
- Small but highly valuable group

### 2. High-Value Loyal
- Recent and frequent buyers
- Strong spending behavior
- Important revenue-driving segment

### 3. Regular Customers
- Moderate recency
- Low frequency
- Average spending
- Largest customer group

### 4. At Risk Customers
- Long time since last purchase
- Low purchase frequency
- High churn probability


---

## Business Recommendations

### VIP / Power Buyers
- Exclusive rewards
- Early access to new products
- Personalized engagement strategies

### High-Value Loyal
- Cross-sell and upsell campaigns
- Loyalty programs

### Regular Customers
- Email nurturing campaigns
- Incentivized repeat purchases

### At Risk Customers
- Re-engagement campaigns
- Time-limited offers
- Win-back promotions


---

## Tools Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn


---


## Key Takeaway

This project demonstrates how transactional data can be transformed into actionable customer intelligence.  

Instead of blanket discounting, businesses can use segmentation to drive targeted, data-driven marketing strategies.
