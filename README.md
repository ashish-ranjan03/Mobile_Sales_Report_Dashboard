# Mobile Sales Analysis Dashboard

A comprehensive Power BI dashboard for analyzing and visualizing mobile phone sales data. This project provides key insights into sales performance, customer behavior, and brand popularity, enabling data-driven decision-making.
---

## 📋 Project Overview

This project aims to provide a clear and interactive overview of mobile sales trends. The dashboard is designed for business stakeholders, including sales managers and marketing teams, to quickly identify top-performing products, understand sales distribution across different regions, and track key performance indicators (KPIs) over time.

### Key Questions Addressed:
* What are the total sales and units sold over a specific period?
* Which mobile brands and models are the top performers?
* What are the sales trends by month, day of the week, and city?
* How do customer ratings correlate with sales?
* What are the most popular payment methods?

---

## 📊 Key Metrics and KPIs

The dashboard focuses on the following core metrics to measure performance:

* **Total Sales**: The total revenue generated from mobile sales (769M).
* **Total Units Sold**: The total number of mobile units sold (19K).
* **Total Transactions**: The total number of sales transactions (4K).
* **Average Selling Price**: The average price of the mobile phones sold (40.17K).
* **Sales vs. Same Period Last Year**: A year-over-year comparison of sales performance.

---

## 📦 Data Source

The dataset for this project is an Excel file (`Mobile Sales Data.xlsx`) containing transactional sales data. The key columns in the dataset include:

* Transaction ID
* Date (Day, Month, Year)
* Brand & Mobile Model
* Units Sold & Price Per Unit
* Customer Details (Name, Age, City)
* Payment Method
* Customer Ratings

---

## 🛠️ Tools Used

* **Power BI**: For data modeling, analysis, and visualization.
* **Power Query**: For data cleaning and transformation (ETL).
* **DAX (Data Analysis Expressions)**: For creating custom calculations and measures.

---

## ⚙️ Data Preparation and Transformation

Before visualization, the raw data was cleaned and transformed using the Power Query Editor in Power BI. The key steps included:

1.  **Date Column Creation**: Combined the `Day`, `Month`, and `Year` columns to create a single `Date` column for time-based analysis.
2.  **Total Sales Column**: Created a new column by multiplying `Units Sold` and `Price Per Unit` to calculate the total sales for each transaction.
3.  **Data Cleaning**: Standardized inconsistent values in the `Day Name` column (e.g., "Sat" to "Saturday").
4.  **Calendar Table**: Created a separate calendar table using DAX to enable advanced time-intelligence analysis, such as Year-over-Year growth.

---

## 📈 DAX Measures

Several DAX measures were created to power the dashboard's visuals. Here are some of the key measures:

* **Total Sales**:
    ```dax
    Total Sales = SUM('Mobile Sales'[Total Sales])
    ```
* **Total Units Sold**:
    ```dax
    Total Units Sold = SUM('Mobile Sales'[Units Sold])
    ```
* **Total Transactions**:
    ```dax
    Transactions = COUNT('Mobile Sales'[Transaction ID])
    ```
* **Sales Same Period Last Year**:
    ```dax
    Total Sales Same Period Last year = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))
    ```

---

## 🎨 Visualizations

The dashboard is composed of three pages with a variety of visualizations to provide a comprehensive view of the data:

* **KPI Cards**: To display the main metrics at a glance.
* **Map**: To show the geographical distribution of sales by city.
* **Donut Chart**: To visualize the distribution of customer ratings.
* **Column and Bar Charts**: To compare sales and units sold by brand, model, month, and day of the week.
* **Matrix**: To provide a detailed, drill-down view of sales performance over time (Year, Quarter, Month).
* **Slicers**: To allow users to filter the data dynamically by brand, model, and payment method.

---

## 🚀 How to Use

1.  **Download the `.pbix` file** from this repository.
2.  **Open the file in Power BI Desktop**.
3.  **Interact with the dashboard** by clicking on different visuals and using the slicers to filter the data.
4.  **Drill down into the data** by right-clicking on the matrix and other visuals to explore deeper insights.

---


