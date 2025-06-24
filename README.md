# amazon_sales
## 🔄 Sales Data Updates and Transformations

This Power BI project focuses on analyzing and visualizing sales performance. Below are the key updates and transformations made to the **Sales Data**:

### 📌 Data Cleaning and Transformation (Power Query)
- Removed null or duplicate rows from the raw sales dataset.
- Converted `Order Date` and `Ship Date` fields to proper `Date` format.
- Standardized `Product Category` and `Customer Region` values using conditional column logic.
- Added a new column for `Order Month` to enable time-based aggregation.

### 📊 Measures and KPIs Created
- **Total Sales** = SUM(`Sales`)
- **Profit Margin** = DIVIDE(SUM(`Profit`), SUM(`Sales`))
- **Average Order Value** = AVERAGE(`Sales`)
- **Sales Growth %** = VAR calc for month-over-month growth

### 🔗 Relationships Established
- Connected `Sales` table to:
  - `Customer` table via `CustomerID`
  - `Product` table via `ProductID`
  - `Calendar` table via `Order Date`

### 📈 Visual Enhancements
- Created slicers for:
  - Product Category
  - Region
  - Year-Month
- Implemented bar charts, line charts, and KPIs for dynamic insights.
- Added tooltips with detailed sales breakdown.

### 📁 Data Model Optimization
- Removed unused columns from large tables.
- Renamed key fields for clarity (e.g., `Cust_ID` → `CustomerID`).
- Enabled star schema for optimal performance.


