# Online Retail Exploratory Data Analysis with Python 


<img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/online%20retail.jpg?raw=true" alt="Online Retail Banner" style="display: block; margin: 0 auto; width: 100%;">



## Table of Contents
1. [Overview](#overview)
2. [Case Study](#case-study)
3. [Prerequisites](#prerequisites)
4. [Project Objectives](#project-objectives)
5. [Dataset](#dataset)
6. [Tasks](#tasks)
    - [Load the Data](#load-the-data)
    - [Data Cleaning](#data-cleaning)
7. [Basic Statistics](#basic-statistics)
8. [Data Visualization](#data-visualization)
    - [Sales Trends Over Time](#sales-trends-over-time)
    - [Top-Selling Products and Countries](#top-selling-products-and-countries)
    - [Outliers and Anomalies](#outliers-and-anomalies)
9. [Conclusions & Key Findings](#conclusions--key-findings)
10. [Business Insights & Recommendations](#business-insights--recommendations)
11. [Tools & Technologies](#tools--technologies)
12. [References](#references)
13. [Contact](#contact)

---

## <span style="color:#2E86C1"><b>Overview</b></span> 

In this project, you will step into the shoes of an entry-level data analyst at an online retail company, helping interpret real-world data to help make a key business decision.

---

## <span style="color:#28B463"><b>Case Study</b></span> 

In this project, you will be working with transactional data from an online retail store. The dataset contains information about customer purchases, including product details, quantities, prices, and timestamps. Your task is to explore and analyze this dataset to gain insights into the store's sales trends, customer behavior, and popular products. 

By conducting exploratory data analysis, you will identify patterns, outliers, and correlations in the data, allowing you to make data-driven decisions and recommendations to optimize the store's operations and improve customer satisfaction. Through visualizations and statistical analysis, you will uncover key trends, such as the busiest sales months, best-selling products, and the store's most valuable customers. Ultimately, this project aims to provide actionable insights that can drive strategic business decisions and enhance the store's overall performance in the competitive online retail market.

---

## <span style="color:#D35400"><b>Prerequisites</b></span> 

Before starting this project, you should have some basic knowledge of Python programming and Pandas. In addition, you may want to use the following packages in your Python environment:

- pandas
- numpy
- seaborn
- matplotlib

These packages should already be installed in Coursera's Jupyter Notebook environment, however if you'd like to install additional packages that are not included in this environment or are working off platform you can install additional packages using `!pip install packagename` within a notebook cell such as:

- `!pip install pandas`
- `!pip install matplotlib`

---

## <span style="color:#8E44AD"><b>Project Objectives</b></span> 

1. Describe data to answer key questions to uncover insights
2. Gain valuable insights that will help improve online retail performance
3. Provide analytic insights and data-driven recommendations

---

## <span style="color:#2E4053"><b>Dataset</b></span>

The dataset you will be working with is the "Online Retail" dataset. It contains transactional data of an online retail store from 2010 to 2011. The dataset is available as a .xlsx file named `Online Retail.xlsx`. 

The dataset contains the following columns:

- InvoiceNo: Invoice number of the transaction
- StockCode: Unique code of the product
- Description: Description of the product
- Quantity: Quantity of the product in the transaction
- InvoiceDate: Date and time of the transaction
- UnitPrice: Unit price of the product
- CustomerID: Unique identifier of the customer
- Country: Country where the transaction occurred

---

## <span style="color:#A93226"><b>Tasks</b></span> 

You may explore this dataset in any way you would like - however if you'd like some help getting started, here are a few ideas:

1. Load the dataset into a Pandas DataFrame and display the first few rows to get an overview of the data.
2. Perform data cleaning by handling missing values, if any, and removing any redundant or unnecessary columns.
3. Explore the basic statistics of the dataset, including measures of central tendency and dispersion.
4. Perform data visualization to gain insights into the dataset. Generate appropriate plots, such as histograms, scatter plots, or bar plots, to visualize different aspects of the data.
5. Analyze the sales trends over time. Identify the busiest months and days of the week in terms of sales.
6. Explore the top-selling products and countries based on the quantity sold.
7. Identify any outliers or anomalies in the dataset and discuss their potential impact on the analysis.
8. Draw conclusions and summarize your findings from the exploratory data analysis.

### <span style="color:#A93226"><b>Load the Data</b></span> 

The dataset was loaded using pandas from an Excel file named Online Retail.xlsx. Below is the initial setup:

This step initializes the environment and provides a quick look at the structure of the dataset before beginning the data exploration and analysis process.

![Load Data](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/Load%20Data..png)



### <span style="color:#A93226"><b>Data Cleaning</b></span> 

Before diving into analysis, it was essential to clean the dataset by addressing missing values and removing redundant or irrelevant columns. This step ensures the quality and reliability of insights derived from the data. Proper data cleaning helps improve performance in both exploratory analysis and any potential machine learning applications.

![Missing Value Analysis](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/missing%20value.png) 

There are 1,454 missing values in the Description column.

There are 135,080 missing values in the CustomerID column — that's a lot! 



To prepare the dataset for analysis, I first checked for missing values. I discovered that the CustomerID column had over 135,000 missing entries, and the Description column had 1,454 missing values. Since these columns are essential for customer segmentation and product-level insights, I removed rows where either CustomerID or Description was missing. I also removed duplicate rows to avoid skewing the analysis. 

### Data Cleaning

| Cleaning Step 1 | Cleaning Step 2 |
|------------------|------------------|
| ![Cleaning 1](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/cleaning.png) | ![Cleaning 2](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/cleaning1.png) | 

dataset is clean! No missing values left

---

## <span style="color:#1F618D"><b>Basic Statistics</b></span> 

To understand the overall structure and distribution of the data, I performed an initial statistical exploration. This included calculating key measures of central tendency (mean, median) and dispersion (standard deviation, min, max, quartiles). These insights provide a solid foundation for identifying patterns, outliers, and potential data quality issues before deeper analysis.

### Basic Statistics

| Statistic 1 | Statistic 2 |
|-------------|-------------|
| ![Basic Statistic](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/basic%20statistic.png) | ![Basic Statistic 1](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/basic%20statistic1.png) | 

📊 Summary Statistics

The dataset contains 401,604 transactions, with noticeable variation in both quantity and unit price:

    Quantity:

        Median: 5 items

        Most common: 1 item

        Mean: 12.18 (with high variability due to outliers like returns or bulk orders)

    Unit Price:

        Median: £1.95

        Most common: £1.25

        Mean: £3.47 (skewed by a few high-priced items)

    Most transactions involve small quantities of low-cost items, though some outliers suggest bulk purchases or data anomalies.



---

## <span style="color:#16A085"><b>Data Visualization</b></span> 

To gain deeper insights into the dataset, I performed exploratory data visualization using matplotlib and seaborn. Visualizations help uncover patterns, trends, and anomalies that may not be obvious through raw statistics alone.

The following aspects were explored:

    Distribution of Unit Price – Understand pricing behavior across products.

    Top 10 Countries by Total Sales – Identify key markets contributing to revenue.

    Top 10 Products by Revenue – Highlight the most profitable items.

    Monthly Sales Trend – Analyze seasonality and performance over time.

These visualizations provide a strong foundation for understanding customer behavior and business performance. 


<div style="display: flex; align-items: center; justify-content: center;">
    <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/raw/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/a1..png" alt="Image 2" style="width: 45%; margin-right: 10px;">
    <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/raw/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/a..png" alt="Image 1" style="width: 45%;">
</div> 

📊 Distribution of Unit Prices (Filtered) – Interpretation

This histogram with KDE (Kernel Density Estimation) shows the distribution of unit prices in the dataset after filtering out extreme outliers. The data is highly right-skewed, indicating that most unit prices are concentrated at the lower end (between 0 and 5), with very few items priced above 20. This suggests that the majority of products are low-cost, and only a small proportion are premium-priced items. This insight can help businesses adjust pricing strategies or identify potential pricing anomalies.


| ![Image 1](https://raw.githubusercontent.com/gerardnynkeu/Portfolio-Data-Analytics/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/b1..png) | ![Image 2](https://raw.githubusercontent.com/gerardnynkeu/Portfolio-Data-Analytics/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/b..png) |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|



### 🌍 Top 10 Countries by Total Sales – Interpretation
The bar chart displays the top 10 countries ranked by total sales. The United Kingdom stands out with an overwhelmingly higher sales volume compared to all other countries, indicating it is the primary market in this dataset. Other countries such as the Netherlands, Ireland (EIRE), Germany, and France follow but contribute significantly less in comparison. This suggests a strong geographic sales concentration, highlighting the UK as a key driver of revenue and a potential focal point for targeted business strategies.


| ![Image 1](https://raw.githubusercontent.com/gerardnynkeu/Portfolio-Data-Analytics/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/c1.png) | ![Image 2](https://raw.githubusercontent.com/gerardnynkeu/Portfolio-Data-Analytics/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/c..png) |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|


### 🏆 Top 10 Products by Revenue – Interpretation
This horizontal bar chart highlights the top 10 best-performing products based on total revenue. The “Regency Cake Stand 3 Tier” is the top revenue generator, significantly outperforming all other products. It is followed by the “White Hanging Heart T-Light Holder” and “Jumbo Bag Red Retrospot.” The chart reveals a concentration of revenue among a few key products, which suggests these items are either high in demand, high in price, or both. This insight can guide inventory planning, marketing focus, and product promotion strategies.


| ![Image 1](https://raw.githubusercontent.com/gerardnynkeu/Portfolio-Data-Analytics/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/d1.png) | ![Image 2](https://raw.githubusercontent.com/gerardnynkeu/Portfolio-Data-Analytics/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/d..png) |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|




### Monthly Sales Trend Analysis

The line chart illustrates the monthly sales trend over a one-year period. Sales began moderately in December, dipped slightly during the first quarter, and showed a noticeable recovery in March and May. Despite minor fluctuations in mid-year, there was a significant increase from August to November, peaking in November with total sales surpassing 1.1 million. However, December experienced a sharp drop. This pattern may reflect seasonal purchasing behavior, possibly linked to holiday sales and year-end consumer trends. Overall, the business appears to experience strong performance in the last quarter of the year.



### <span style="color:#16A085"><b>Sales Trends Over Time</b></span>
Analyze sales trends and identify busy months and days of the week.

<p align="center">
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/e1.png" alt="Image 1" width="45%" />
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/e..png" alt="Image 2" width="45%" />
</p> 



### Total Sales by Month

This bar chart shows the total monthly sales from December 2010 through December 2011. Sales remained relatively stable during the first half of 2011, fluctuating between approximately 430,000 and 650,000. A strong upward trend began in August, with a notable peak in November 2011 reaching over 1.1 million. This spike may reflect seasonal demand, such as holiday shopping or promotional events. Interestingly, sales dropped sharply in December 2011, which could suggest a shift in consumer behavior or reporting timing. Overall, the business demonstrated strong growth momentum in the final quarter of the year.


### <span style="color:#16A085"><b>Top-Selling Products and Countries</b></span>
Discover the products and countries with the highest sales.


<p align="center">
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/f1.png" alt="Image 1" width="45%" />
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/f..png" alt="Image 2" width="45%" />
</p> 


### Total Sales by Day of the Week

The bar chart reveals how sales are distributed across the days of the week. Thursday stands out as the most profitable day, with total sales nearing 1.9 million. Tuesday and Wednesday also perform strongly, followed by Monday and Friday with moderate sales levels. Notably, Sunday records the lowest total sales, while Saturday shows no data—possibly indicating either no sales or missing data for that day. This trend suggests that customer activity is highest during weekdays, particularly mid-week, which could inform staffing, marketing campaigns, or inventory planning.



<p align="center">
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/g1.png" alt="Image 1" width="45%" />
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/g..png" alt="Image 2" width="45%" />
</p> 





Here's a short interpretation:

This bar chart visualizes the top 10 best-selling products by quantity. The data shows that "WORLD WAR 2 GLIDERS ASSTD DESIGNS" is the most sold item, with over 50,000 units sold. It is followed by "JUMBO BAG RED RETROSPOT" and "ASSORTED COLOUR BIRD ORNAMENT", which also demonstrate high sales figures. The chart reveals a gradual decline in quantities sold among the top 10 products, with "PACK OF 60 PINK PAISLEY CAKE CASES" rounding out the list. This analysis helps identify customer preferences and high-demand items, which can guide inventory planning and marketing strategies.



<p align="center">
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/h1.png" alt="Image 1" width="45%" />
  <img src="https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/Online%20Retail%20Exploratory%20Data%20Analysis%20Python/h..png" alt="Image 2" width="45%" />
</p> 



Here's a concise interpretation:

This bar chart displays the top 10 countries by total quantity of products sold. The United Kingdom overwhelmingly leads in sales, with over 4 million units sold—far surpassing all other countries. The Netherlands, EIRE (Ireland), and Germany follow, but with significantly smaller volumes. This suggests that the business is primarily driven by the UK market, while international sales remain relatively modest. These insights highlight the importance of focusing on the UK for core operations, while also presenting opportunities to expand market presence abroad.



### <span style="color:#16A085"><b>Outliers and Anomalies</b></span>
Identify and discuss the impact of outliers on the analysis.

---

## <span style="color:#7D3C98"><b>Conclusions & Key Findings</b></span>
Summarize the key findings from the exploratory data analysis.

---

## <span style="color:#148F77"><b>Business Insights & Recommendations</b></span>
Provide actionable insights and recommendations based on the analysis.

---

## <span style="color:#CA6F1E"><b>Tools & Technologies</b></span>
List of tools and technologies used in this project.

---

## <span style="color:#B03A2E"><b>References</b></span>
Provide references to any sources, libraries, or datasets used.

---

## <span style="color:#566573"><b>Contact</b></span>
Feel free to reach out for further information:
- **Author**: Gerard Nynkeu
- **GitHub**: [gerardnynkeu](https://github.com/gerardnynkeu)
- **Email**: [Your Email Here]
