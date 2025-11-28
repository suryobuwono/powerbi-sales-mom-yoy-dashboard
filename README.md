# Power BI Sales Dashboard: Dynamic MoM & YoY Analysis

![alt text](DashboardOverview.gif)

## 1. Introduction
This Power BI dashboard was designed to provide a multi-layered financial overview of sales performance. The analysis starts at a high level, comparing **Current Year trends against Previous Year performance** to gauge annual health, before drilling down into granular **Month-over-Month (MoM)** analysis.

The primary objective is to enable data-driven decision-making by identifying macro trends (Yearly) and micro movements (Monthly), spotting which product sub-categories are driving growth versus those that are dragging down profitability.

### Target Audience
- **Executive Management:** For high-level annual performance tracking (Current Year vs. Last Year).

- **Sales Managers:** To identify specific months with "Strong Upward Trends" or "Declines."

- **Financial Analysts:** To investigate profit margins, sales drivers, and correlation between discounts and profit using dynamic scatterplots.

## 2. Skills Showcased
This project demonstrates an end-to-end Power BI development workflow, highlighting advanced interactivity and complex DAX logic.

### 🛠 Technical Implementation
- **Parameters & Dynamic Logic**
   - **Field Parameters:** Implemented to allow dynamic X-axis selection on scatterplots, enabling users to swap analysis between Sales, Profit, or Units Sold without needing multiple charts.

   - **Numeric Parameters:** Used to filter years and drive conditional calculations for Current Year vs. Previous Year trend lines.

- **Advanced DAX**
    - **Time Intelligence:** Used `DATEADD` and `CALCULATE` for seamless Month-over-Month and Year-over-Year comparisons.

    - **Error Handling & Math Logic:** Created robust measures to handle **Negative Denominators** in profit growth calculations (switching from % to Absolute `$` change) and Capping Logic (`MIN`/`MAX`) to limit percentage growth to $\pm 1000\%$ for readability.

    - **Dynamic UX:** Used `HASONEVALUE` to create call-to-action text (e.g., "Select a month to view value") that changes based on user interaction.

- **Power Query (ETL)**
    - Data cleaning and transformation from raw CSV files.

    - Created a dedicated **Date Dimension** (`date_dim`) and custom sorting logic for product categories.

- **Data Modeling** 
    - Built a **Star Schema** connecting the Fact table (`orders_fact`) to Dimension tables (`products_dim`, `date_dim `, `customers_dim`, `location_dim`_).

### 🎨 Visualization & UX

- **Interactive Buttons & Page Navigation:** Created a seamless experience, allowing users to switch the Matrix view between Sales Growth, Profit Growth, and Quantity Growth with a single click.

- **Conditional Formatting:** Applied dynamic icon indicators based on performance thresholds.

- **Cross-Filtering:** Configured visuals to interact intuitively.

## 3. Key Metrics & Analyses
The dashboard focuses on three core pillars of retail performance: **Sales**, **Profit**, and **Quantity**.

### 📊 Analytical Features
- **Year-over-Year (YoY) Comparison:** Visualizes the trajectory of the current year against the previous year.

- **MoM Growth Analysis:** Calculates the variance between the current month and the previous month with dynamic status indicators.

- **Correlation Analysis:** A scatterplot to analyze the relationship between Discount Rates and key metrics (Sales/Profit/Quantity).

- **Ranking Analysis:** A sorted bar chart identifying the highest revenue-generating products in hierarchy (categories → subcategories → products).

## 4. Dashboard Preview
![alt text](<Preview 1.png>)

![alt text](<Preview 2.png>)

![alt text](<Preview 3.png>)

![alt text](<Preview 4.png>)

## 5. How to Use
1. Clone this repository or download the `SalesDashboard_by_SuryoBuwono.pbix` file directly. 
2. Open the file in **Power BI Desktop**.
3. Interact with the dashboard.

## 6. References
**Dataset:** [Data with Baraa](https://www.datawithbaraa.com/wiki/tableau#welcome-to-tableau-course)

## 7. Authorship & Contact Information

**Created by:** S.B. Suryo Buwono

**Tools:** Microsoft Power BI

**Last Updated:** November 28, 2025

> For inquiries, collaboration, or feedback regarding this dashboard, please feel free to reach out: 
>
>**📧 Email:** mail.suryobuwono@gmail.com