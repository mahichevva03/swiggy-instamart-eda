# 🛵 Swiggy Instamart Operations & Revenue Analysis

**Tool:** Python (Pandas, Matplotlib, Seaborn)  
**Author:** [Maheshwari Chevva](https://github.com/mahichevva03)  
**LinkedIn:** [linkedin.com/in/maheshwari-chevva-6320372a9](https://www.linkedin.com/in/maheshwari-chevva-6320372a9)

---

## 📌 Project Objective

An end-to-end exploratory data analysis (EDA) on Swiggy Instamart order data to uncover operational inefficiencies and revenue patterns. The goal was to answer key business questions around delivery performance, customer ordering behaviour, product demand, and payment preferences.

---

## 📊 Dataset

**File:** `swiggy_instamart.csv`  
**Features include:**

| Column | Description |
|---|---|
| `order_id` | Unique order identifier |
| `order_date` | Date of order placement |
| `order_time` | Time of order placement |
| `product_name` | Product ordered |
| `category` | Product category |
| `quantity` | Units ordered |
| `final_price` | Order value |
| `delivery_time_min` | Delivery duration in minutes |
| `area` | Delivery location |
| `payment_mode` | Payment method used |
| `order_status` | Delivered / Cancelled / Pending |
| `rating` | Customer rating |

---

## 🔍 Analysis Performed

### Data Cleaning
- Removed duplicate records
- Parsed `order_date` to datetime format
- Converted `delivery_time_min`, `final_price`, `rating` to numeric
- Handled null values across key columns

### Feature Engineering
- Extracted `order_hour` from order time
- Extracted `day_name` from order date
- Created `delivery_bucket` (0-10, 11-15, 16-20, 21-30, 30+ minutes)
- Computed `revenue` from final price

### Business Questions Answered
1. What is the total revenue and total number of unique orders?
2. Which product categories generate the most revenue?
3. What are the top 10 most ordered products by quantity?
4. Which hours of the day see peak order volumes?
5. Which areas have the slowest average delivery times?
6. What payment modes do customers prefer?
7. What is the distribution of order statuses?

---

## 📈 Visualizations

| Chart | Insight |
|---|---|
| Bar chart — Revenue by Category | Identifies top-performing product segments |
| Bar chart — Top 10 Products by Quantity | Most in-demand SKUs |
| Line chart — Orders by Hour | Peak ordering windows |
| Bar chart — Avg Delivery Time by Area | Slowest delivery zones |
| Count plot — Payment Mode Usage | Preferred payment methods |

---

## 💡 Key Findings

- Peak order volume occurs in specific hours (late morning and evening)
- Certain areas consistently show higher average delivery times
- A small number of product categories drive the majority of revenue
- UPI / digital payments are the dominant payment mode

---

## 🛠️ Libraries Used

```python
pandas · numpy · matplotlib · seaborn · warnings · os
```

---

## 📁 Files

| File | Description |
|---|---|
| `swiggy.ipynb` | Full EDA notebook |

---

## 🚀 How to Run

1. Clone the repository
2. Place `swiggy_instamart.csv` in the same directory
3. Open `swiggy.ipynb` in Jupyter Notebook or VS Code
4. Run all cells sequentially
