# Olist-E-Commerce-Data-Analysis
A comprehensive Exploratory Data Analysis (EDA) project on the Olist E-Commerce dataset. The project analyzes orders, sales, customers, products, sellers, payments, delivery performance, and customer reviews to discover business insights and provide data-driven recommendations.

## 📊 Dataset

If you would like the dataset used in this project, feel free to connect with me on LinkedIn:

🔗 **LinkedIn:** [Mayank Bhatt](YOUR_LINKEDIN_PROFILE_URL)

Feel free to message me, and I'll be happy to share the dataset.

# Olist E-Commerce Data Analysis

## 📌 Project Overview

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on the Olist E-Commerce dataset.

The main goal of this project is to understand the overall business performance and discover useful insights related to:

- Orders
- Sales and Revenue
- Customers
- Products
- Sellers
- Payments
- Delivery Performance
- Customer Reviews

The analysis also explores relationships between different business variables such as delivery time, review scores, product price, freight cost, product weight, and payment installments.

---

# 📂 Dataset

The dataset contains multiple tables related to an e-commerce platform.

### Tables Used

- `customers`
- `locations`
- `orders`
- `items`
- `payments`
- `reviews`
- `products`
- `sellers`
- `category_translation`

These tables were analyzed individually and connected using common IDs such as:

- `customer_id`
- `order_id`
- `product_id`
- `seller_id`

---

# 🧹 Data Cleaning

Before starting the analysis, several data quality checks were performed.

### 1. Missing Values

Missing values were checked across all tables.

Some missing values were found in:

- Order approval and delivery dates
- Product information
- Review comments

The missing values in delivery-related columns were mostly connected to canceled, unavailable, or incomplete orders. These values were kept where they represented valid business situations.

---

### 2. Duplicate Values

Duplicate rows were checked across all datasets.

The `locations` dataset contained duplicate records, which were removed to reduce unnecessary repetition.

Other tables did not contain duplicate rows.

---

### 3. Date Conversion

Date columns were converted into proper datetime format.

This allows easier analysis of:

- Order trends
- Monthly sales
- Delivery time
- Approval time
- Estimated vs actual delivery

---

### 4. Inconsistent Text Values

Text columns such as cities, states, payment types, and order statuses were checked.

Some city names contained spelling or accent differences, such as:

- `sao paulo`
- `são paulo`

Text values were standardized where necessary to improve the accuracy of grouping and analysis.

---

### 5. Invalid Values

The datasets were checked for invalid values such as:

- Negative prices
- Negative freight values
- Zero payments
- Invalid review scores
- Invalid product dimensions

No major negative or impossible values were found.

Some zero values were identified, such as:

- Zero freight values
- Zero payment values
- Zero product weights
- Zero payment installments

These records were investigated because some may represent valid business cases, vouchers, discounts, or data quality issues.

---

### 6. Outlier Detection

Outliers were checked using the IQR method for:

- Product price
- Freight value
- Payment value
- Product weight
- Product dimensions

Several outliers were found.

These values were not automatically removed because they may represent genuine expensive products, heavy products, or unusual customer orders.

---

### 7. Relationship and Merge Key Validation

Relationships between tables were checked to make sure the datasets could be merged correctly.

The following relationships were verified:

- Customers ↔ Orders
- Orders ↔ Items
- Orders ↔ Payments
- Orders ↔ Reviews
- Items ↔ Products
- Items ↔ Sellers
- Products ↔ Category Translation

Most IDs connected correctly between tables.

Some orders did not have items, payments, or reviews, which was mainly related to canceled, unavailable, or incomplete orders.

---

# 📊 Exploratory Data Analysis

The analysis was divided into several sections.

## 1. Overall Business Overview

The overall structure of the business was analyzed using:

- Total Orders
- Total Customers
- Total Products
- Total Sellers
- Total Revenue
- Average Order Value
- Order Status Distribution

This provides a high-level understanding of the business.

---

## 2. Order Analysis

Order data was analyzed to understand:

- Order status distribution
- Order trends over time
- Monthly order volume
- Successful vs unsuccessful orders
- Purchase patterns

Most orders in the dataset were successfully delivered.

---

## 3. Sales and Revenue Analysis

Sales and revenue analysis focused on:

- Total sales
- Revenue trends
- Top product categories
- High-value orders
- Average order value

This helps identify the products and categories that contribute the most to business revenue.

---

## 4. Customer Analysis

Customer behavior was analyzed using:

- Customer location
- Top customer states
- Top customer cities
- Purchase frequency
- Repeat customers

The analysis showed that most customers made only one purchase.

This suggests that there is an opportunity to improve **customer retention** and encourage repeat purchases.

---

## 5. Product Analysis

Product analysis included:

- Product category distribution
- Top-selling categories
- Product price
- Product weight
- Product dimensions

The analysis helps understand which types of products are most important to the business.

---

## 6. Seller Analysis

Seller performance was analyzed using:

- Number of orders
- Number of products sold
- Seller locations
- Sales contribution
- Delivery performance

This can help identify high-performing sellers and sellers that may require improvement.

---

## 7. Payment Analysis

Payment data was analyzed to understand:

- Most commonly used payment methods
- Payment values
- Number of installments
- Relationship between payment value and installments

Credit cards were the most commonly used payment method.

A moderate positive relationship was found between payment value and the number of installments.

---

## 8. Delivery Analysis

Delivery performance was analyzed using:

- Delivery time
- Estimated delivery time
- Actual delivery date
- Delayed deliveries

Delivery time is an important factor because it can directly affect customer satisfaction.

---

## 9. Review Analysis

Customer reviews were analyzed using:

- Review score distribution
- Average review score
- Relationship between delivery time and review score

A negative relationship was found between delivery time and review score.

This means that customers generally tend to give lower ratings when delivery takes longer.

---

# 🔍 Advanced Relationship Analysis

Several relationships between important business variables were explored.

## Delivery Time vs Review Score

A negative correlation was found between delivery time and review score.

**Conclusion:** Longer delivery times are generally associated with lower customer ratings.

---

## Order Value vs Review Score

A weak negative relationship was found between order value and review score.

**Conclusion:** Spending more money does not necessarily result in a better customer experience or higher review score.

---

## Product Price vs Freight Value

A moderate positive relationship was found between product price and freight value.

**Conclusion:** More expensive products may have higher shipping costs, but the relationship is not perfect.

---

## Product Weight vs Freight Value

A positive relationship was found between product weight and freight value.

**Conclusion:** Heavier products generally tend to have higher shipping costs.

---

## Payment Value vs Number of Installments

A moderate positive relationship was found between payment value and the number of installments.

**Conclusion:** Customers making larger payments are more likely to use multiple installments.

---

# 💡 Key Business Insights

- Most orders were successfully delivered.
- Delivery performance has an important impact on customer satisfaction.
- Longer delivery times are generally associated with lower review scores.
- Most customers made only one purchase.
- Customer retention can be improved.
- Credit cards were the most commonly used payment method.
- Product price and freight value show a moderate positive relationship.
- Heavier products generally have higher shipping costs.
- High-value orders do not always receive better customer reviews.
- Some outliers represent unusual but potentially valid business cases.

---

# 🚀 Business Recommendations

### Improve Delivery Performance

Focus on reducing delivery delays and improving logistics because faster delivery is associated with better customer review scores.

### Improve Customer Retention

Since most customers made only one purchase, the business can introduce:

- Loyalty programs
- Personalized offers
- Discounts
- Product recommendations

to encourage repeat purchases.

### Monitor High-Value Orders

Customers spending more money may have higher expectations. High-value orders should receive additional attention to ensure a better customer experience.

### Optimize Freight Costs

Products with unusually high freight values should be investigated to identify opportunities for better logistics and shipping optimization.

### Monitor Seller Performance

Sellers can be evaluated based on:

- Sales
- Number of orders
- Delivery performance
- Customer review scores

High-performing sellers can be used as benchmarks for improving other sellers.

### Investigate Low Review Scores

Low-rated orders should be analyzed further to identify whether the main reasons are:

- Delivery delays
- Product quality
- Seller performance
- Customer expectations

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

# 📈 Future Improvements

This project can be improved further by:

- Creating an interactive Power BI dashboard
- Building a customer segmentation model
- Performing RFM analysis
- Predicting customer review scores
- Predicting delivery delays
- Analyzing customer retention in more detail
- Creating seller performance scores
- Building machine learning models for business predictions

---

# 📁 Project Structure

```text
Olist-E-Commerce-Data-Analysis/
│
├── data/
│   └── Dataset files
│
├── notebooks/
│   └── Olist_Ecommerce_EDA.ipynb
│
├── images/
│   └── Visualizations and charts
│
├── README.md
└── requirements.txt
