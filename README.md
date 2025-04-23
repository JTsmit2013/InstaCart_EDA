# 📦 InstaCart EDA (TripleTen Sprint 2)
**Analyzing Instacart Customer Ordering Trends**

## 🧠 Project Overview
This exploratory data analysis (EDA) investigates customer behavior and ordering trends on Instacart. The goal is to uncover actionable insights that can help optimize inventory management, boost customer satisfaction, and better understand purchasing patterns.

## 📊 Datasets Used
1. **`instacart_orders_df`** – Order behavior per user:
   - `order_dow`: Day of the week (0=Sunday).
   - `days_since_prior_order`: Days since the previous order (includes missing values).

2. **`products_df`** – Product names and their aisle assignments.

3. **`aisles_df`** – Aisle IDs and names.

4. **`departments_df`** – Department IDs and item categories.

5. **`order_prod_df`** – Links products to orders, including:
   - Reorder status.
   - Position in cart (`add_to_cart_order`).

## 🛠 Libraries Used
- **Pandas** – Data cleaning & manipulation  
- **NumPy** – Numeric operations  
- **Plotly Express** – Interactive plots  
- **Matplotlib** – Static visualizations  

## 🎯 Goals
- Clean and structure all datasets.
- Identify and resolve duplicates and missing values.
- Visualize:
  - Order volume by time of day and weekday
  - Top reordered products
  - Typical cart size and reorder rates

## 🧹 Data Cleaning Highlights
### `instacart_orders_df`
- Removed duplicate orders (common on Wednesdays at 2 AM).
- Mapped `order_dow` to weekday names.

### `products_df`
- Fixed typos and removed duplicate/missing names (especially in aisle 100).
- Dropped rows labeled "unknown."

### `departments_df` & `aisles_df`
- Verified all department and aisle IDs/names were unique and accurate.

### `order_prod_df`
- Checked for duplicate (order, product) pairs — none found.
- Retained missing `add_to_cart_order` entries for further analysis.

## 🔍 Early Insights
- Cleaned datasets are now consistent and analysis-ready.
- Time-based order patterns and reorder rates reveal customer loyalty and behavior.
- Frequent reorders suggest clear stock priorities.

## 📈 Next Steps
- Build visualizations to explore:
  - Order volume by hour and weekday.
  - Most popular and most reordered products.
  - Average order size and reorder percentages.
- Translate patterns into stocking and marketing recommendations.
  
## ▶️ How to Run
1. Clone this repository.
2. Install required libraries: `pandas`, `numpy`, `plotly`, `matplotlib`.
3. Place dataset files in the `datasets` directory.
4. Execute the Jupyter Notebook to clean and analyze the data.
