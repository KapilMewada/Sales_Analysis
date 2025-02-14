# Sales Analysis Project

## 📌 Overview
The **Sales Analysis Project** aims to analyze sales data from two different CSV files: `sale.csv` and `menu.csv`. The analysis focuses on customer spending patterns, category-wise sales, time-based trends, and geographical performance.

## 📂 Data Sources
We have two datasets:

### 📄 `sale.csv`
Contains sales transaction details.

| Column Name  | Description |
|-------------|-------------|
| `sale_id`     | Unique transaction ID |
| `customer_id` | ID of the customer |
| `product_id`  | ID of the purchased product |
| `quantity`    | Number of units purchased |
| `price`       | Price per unit |
| `timestamp`   | Date and time of purchase |
| `country`     | Country where the sale occurred |
| `source`      | Sales channel (e.g., online, offline) |

### 📄 `menu.csv`
Contains product details.

| Column Name  | Description |
|-------------|-------------|
| `product_id`  | Unique product identifier |
| `category`    | Category of the product |
| `product_name` | Name of the product |

## 🔄 Data Transformation & Feature Engineering

1. **📅 Add Time-Based Columns** to the `sale.csv` dataset:
   - **Year**: Extracted from the `timestamp` column.
   - **Month**: Extracted from the `timestamp` column.
   - **Quarter**: Derived from the month.

2. **💰 Total Amount Spent by Each Customer**
   - Aggregated total spending per customer by multiplying `quantity * price`.

3. **🍽️ Total Amount Spent by Food Category**
   - Merged `sale.csv` with `menu.csv` on `product_id`.
   - Aggregated sales per category.

4. **📊 Total Amount Spent in Each Month**
   - Grouped sales by `Year` and `Month`.

5. **🌍 Total Sales in Each Country**
   - Grouped sales data by `Country`.

6. **🛒 Total Sales by Each Source**
   - Aggregated sales based on `source` (Online, Offline, etc.).

## 🛠 Technologies Used
- **Apache Spark (PySpark)** for data processing
- **Pandas** for small-scale analysis
- **Jupyter Notebook** for interactive exploration
- **Matplotlib & Seaborn** for visualization

## 🚀 Execution Steps
1. Load `sale.csv` and `menu.csv` into PySpark DataFrames.
2. Perform necessary transformations and aggregations.
3. Generate insights and visualizations.
4. Save results in CSV or database for reporting.

## 📈 Results & Insights
- Identified top-spending customers.
- Analyzed seasonal trends in sales.
- Evaluated best-performing product categories.
- Determined high-revenue countries and sales channels.

## 🔮 Future Improvements
- Implement real-time data ingestion.
- Enhance visualization with interactive dashboards.
- Use machine learning to predict sales trends.

---
### ✍️ Author: Kapil Mewada
📅 *Date: 02.14.2025


