# InstaCart_EDA
# Instacart Customer Data Ordering Trends

## Overview
This project explores ordering trends from Instacart customer data to provide insights that help optimize stock, enhance customer satisfaction, and understand customer behavior. The analysis uses five datasets containing order, product, aisle, department, and reorder information.

## Datasets
1. **`instacart_orders_df`**: Customer ordering habits, including:
   - `order_dow`: Day of the week the order was placed.
   - `days_since_prior_order`: Days since the previous order (with missing values).
2. **`products_df`**: Product details such as names and associated aisles.
3. **`aisles_df`**: Information on aisles and their associated products.
4. **`departments_df`**: Department details and item categorization.
5. **`order_prod_df`**: Tracks product reorder status and cart placement.

## Libraries Used
- **Pandas**: Data manipulation and cleaning.
- **NumPy**: Scientific computing.
- **Plotly Express**: Interactive visualizations.
- **Matplotlib**: Static visualizations.

## Goals
1. Clean and preprocess the data by:
   - Removing duplicates.
   - Handling missing values.
2. Visualize key trends:
   - Distribution of orders by time of day and day of the week.
   - Most frequently ordered and reordered products.
   - Typical order size and reorder proportions.
3. Analyze customer behavior to inform Instacart and stores on stocking decisions.

## Data Cleaning Process
### `instacart_orders_df`
- Found and removed duplicates (notably many orders on Wednesdays at 2:00 AM).
- Mapped `order_dow` to weekday names for clarity.

### `products_df`
- Identified and removed duplicate product names.
- Fixed misspellings and missing values in product names, particularly in aisle 100.
- Removed rows labeled "unknown."

### `departments_df`
- Verified no duplicates in department IDs or names.

### `aisles_df`
- Confirmed no duplicates in aisle data or IDs.

### `order_prod_df`
- Checked for duplicates in `order_id` and `product_id` combinations; none found.
- Retained rows with missing `add_to_cart_order` values for further analysis.

## Key Insights
1. **Duplicates**:
   - Removed duplicates across datasets.
   - Corrected product name and aisle anomalies.
2. **Missing Data**:
   - Addressed missing values in `products_df` and `order_prod_df`.
3. **Initial Visualizations**:
   - Histograms and data summaries highlight trends in ordering times, products, and customer preferences.

## Next Steps
- Create detailed histograms and visualizations to illustrate:
  - Order distributions by time and day.
  - Frequency of reordered products.
  - Average order sizes.
- Use findings to recommend stocking strategies and improve customer satisfaction.

## How to Run
1. Clone this repository.
2. Install required libraries: `pandas`, `numpy`, `plotly`, `matplotlib`.
3. Place dataset files in the `datasets` directory.
4. Execute the Jupyter Notebook to clean and analyze the data.
