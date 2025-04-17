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

Quantity:

Count: 401,604 records, which is the total number of transactions.

Mean: The average quantity purchased per transaction is 12.18.

Standard Deviation: A high standard deviation (250.28) suggests significant variation in the quantity of items purchased per transaction.

Min: The minimum quantity is -80,995, which likely indicates an error (possibly a return or refund).

25th Percentile (Q1): 25% of transactions involve purchasing 2 or fewer items.

50th Percentile (Median): The median quantity is 5, meaning half of the transactions have 5 or fewer items.

75th Percentile (Q3): 75% of transactions involve purchasing 12 or fewer items.

Max: The maximum quantity is 80,995, which is an outlier, likely indicating a bulk purchase.
UnitPrice:

Count: 401,604 records.

Mean: The average unit price of items is 3.47, which suggests most items are priced affordably.

Standard Deviation: The standard deviation (69.76) indicates there’s a wide range of item prices, likely due to a few high-priced items.

Min: The minimum price is 0, which could indicate free items or missing price data.

25th Percentile (Q1): 25% of items have a unit price of 1.25 or less.

50th Percentile (Median): The median price is 1.95, meaning half of the items are priced below this value.

75th Percentile (Q3): 75% of items are priced below 3.75.

Max: The highest unit price is 38,970, which could be a luxury or high-end item, or it may indicate an error.
Summary:

The data shows significant variation in both quantities and prices, with a few extreme values (negative quantities and very high prices), which may require further cleaning or investigation.

The majority of transactions involve low-priced items in small quantities, but there are some outliers with very large quantities and high-priced items. 



Here’s a brief interpretation of the median and mode values: Median:

Median Quantity: 5.0 – Half of the transactions involve purchasing 5 or fewer items, showing that most purchases are on the smaller side, but not too small.

Median Unit Price: 1.95 – Half of the items are priced below 1.95, indicating that the majority of items are relatively low-priced.
Mode:

Mode Quantity: 1 – The most common quantity purchased in a transaction is 1 item, which suggests that many purchases are single-item transactions.

Mode Unit Price: 1.25 – The most common unit price is 1.25, showing that a significant portion of items are priced at this value.
Summary:

Most transactions tend to involve purchasing one item, and these items are typically priced at 1.25. However, when looking at the broader dataset, the median indicates that many transactions involve slightly more items (around 5), with a price point around 1.95. This suggests a mix of small, low-priced purchases and occasional larger purchases.



---

## <span style="color:#16A085"><b>Data Visualization</b></span>
Generate plots to visualize the dataset and uncover trends.
### <span style="color:#16A085"><b>Sales Trends Over Time</b></span>
Analyze sales trends and identify busy months and days of the week.

### <span style="color:#16A085"><b>Top-Selling Products and Countries</b></span>
Discover the products and countries with the highest sales.

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
