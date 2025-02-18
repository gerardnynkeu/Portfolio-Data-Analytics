# Marketing Sales Analysis

![Marketing Sales Analysis](data-analysis-intro.png) 


# Table of Contents  

- [Introduction](#Introduction)
- [ Dataset Description](#Dataset-Description)
- [  Dataset Overview](#Dataset-Overview)
- [Step 1: Imports and Data Loading](#step-1-imports-and-data-loading)  
  - [1.1 Import Libraries](#11-import-libraries)  
  - [1.2 Load Dataset](#12-load-dataset)  

- [Step 2: Data Exploration](#step-2-data-exploration)  
  - [2.1 Display First 10 Rows](#21-display-first-10-rows)  
  - [2.2 Dataset Dimensions](#22-dataset-dimensions)  
  - [2.3 Check Missing Values](#23-check-missing-values)  
  - [2.4 Handle Missing Values](#24-handle-missing-values)  
  - [2.5 Pairwise Relationships](#25-pairwise-relationships)  

- [Step 3: Model Building](#step-3-model-building)  
  - [3.1 Select Relevant Columns](#31-select-relevant-columns)  
  - [3.2 Linear Regression Formula](#32-linear-regression-formula)  
  - [3.3 Fit the Model](#33-fit-the-model)  

- [Step 4: Results and Evaluation](#step-4-results-and-evaluation)  
  - [4.1 Model Summary](#41-model-summary)  
  - [4.2 Key Coefficients](#42-key-coefficients)  
  - [4.3 Regression Plot](#43-regression-plot)  
  - [4.4 Residual Distribution](#44-residual-distribution)  
  - [4.5 Q-Q Plot for Normality](#45-q-q-plot-for-normality)  
  - [4.6 Scatterplot of Residuals](#46-scatterplot-of-residuals)  

- [Step 5: Conclusion](#step-5-conclusion)  
  - [5.1 Key Takeaways](#51-key-takeaways)  
  - [5.2 Framing Findings for Stakeholders](#52-framing-findings-for-stakeholders)  
  - [5.3 Framing the Findings for External Stakeholders](#53-framing-the-findings-for-external-stakeholders)

- [Step 6: Key Questions Answered](#step-6-Key-Questions-Answered)

  
 



- [Connect with Me](#connect-with-me)  




## Introduction

Analyzing the Impact of Influencer Marketing with Simple Linear Regression

In this project, I worked as part of an analytics team tasked with delivering insights about our company's sales and marketing practices. My specific focus was on exploring the use of influencer marketing and analyzing its effectiveness in driving sales.

To achieve this, I employed simple linear regression to model the relationship between the radio promotion budget and sales revenue. This approach allowed me to assess both the direction and magnitude of the relationship between these variables, uncovering patterns that could guide data-driven decisions.

The dataset provided contained detailed information about various marketing campaigns, including investments in TV, radio, and social media promotions, as well as the corresponding revenue generated. By analyzing this data, I aimed to provide company leaders with actionable insights to optimize future marketing strategies.

The ultimate goal was to help decision-makers allocate resources more effectively by identifying which marketing channels deliver the highest return on investment. This project demonstrated the power of simple linear regression in transforming large datasets into meaningful insights, enabling better predictions and strategic decision-making. 



## Dataset Description 

This dataset contains information on sales performance and marketing expenditures across different advertising channels. It includes 572 observations and 5 variables, described as follows:

TV (categorical: "Low", "Medium", "High"): Level of investment in TV advertising.
Radio (numeric: float): Amount spent on radio advertising.
Social Media (numeric: float): Amount spent on social media advertising.
Influencer (categorical: "Mega", "Macro", "Micro"): Type of influencer used in the campaign.
Sales (numeric: float): Total sales generated. 

[Download the dataset](marketing-sales-data.csv)


##  Dataset Overview 

Total Entries: 572
Missing Values:
TV: 1 missing value
Radio: 1 missing value
Sales: 1 missing value
Descriptive Statistics:
Radio: Mean ≈ 18.65, Min ≈ 0.19, Max ≈ 48.87
Social Media: Mean ≈ 3.25, Min ≈ 0.01, Max ≈ 11.26
Sales: Mean ≈ 193.52, Min ≈ 31.20, Max ≈ 358.42 


## Step 1: Imports and Data Loading  

- **1.1 Import Libraries**  
- **1.2 Load Dataset**

Before working with the dataset, we import necessary Python libraries such as pandas, numpy, seaborn, matplotlib, and statsmodels. 
The dataset is loaded into a Pandas DataFrame and reviewed for initial exploration.


![Marketing Sales Analysis](import-load-data.png) 



## Step 2: Data Exploration  

In this step, we analyze the dataset to understand its structure, detect missing values, and examine relationships between variables. This helps in identifying patterns, potential issues, and key insights before further analysis.  

- **2.1 Display First 10 Rows** – Preview the first few rows to get an overview of the dataset.  
- **2.2 Dataset Dimensions** – Check the number of rows and columns to understand the dataset size.  
- **2.3 Check Missing Values** – Identify any missing data that may need to be handled.  
- **2.4 Handle Missing Values** – Apply strategies to deal with missing data (e.g., imputation or removal).  
- **2.5 Pairwise Relationships** – Explore relationships between variables using visualizations.  



![Marketing Sales Analysis](EDA.png) 



I also use visualization techniques such as pairplots to explore relationships between features.


![Marketing Sales Analysis](3.5-Pairwise-Relationships.png) 

## Step 3: Model Building  

The process of creating, training, and validating mathematical or machine learning models to analyze data, make predictions, or solve specific problems. It involves selecting appropriate algorithms, preparing data, and tuning parameters to achieve optimal performance and accuracy.  

- **3.1 Select Relevant Columns** – Choosing the independent and dependent variables for the regression model.  
- **3.2 Linear Regression Formula** – Defining the regression equation to be fitted to the data.  
- **3.3 Fit the Model** – Training the linear regression model using `statsmodels`.



![Marketing Sales Analysis](model-building.png) 







## Step 4: Results and Evaluation  

In this step, I evaluate the performance of my regression model by analyzing key metrics and visualizations. I check how well the model fits the data, identify potential issues, and ensure its reliability for making predictions. I examine the model summary, key coefficients, and various plots to assess residuals and validate assumptions like normality and homoscedasticity. This step helps me determine if my model is effective or needs further improvements before using it for decision-making. 🚀

- **4.1 Model Summary** – Generating a summary of the fitted model to interpret results.  
- **4.2 Key Coefficients** – Extracting and analyzing the key coefficients of the regression model.  
- **4.3 Regression Plot** – Visualizing the regression line and the relationship between variables.  
- **4.4 Residual Distribution** – Analyzing the distribution of residuals to check for normality.  
- **4.5 Q-Q Plot for Normality** – Using a Q-Q plot to further assess the normality of residuals.  
- **4.6 Scatterplot of Residuals** – Plotting residuals against predicted values to check for patterns or heteroscedasticity.


![Marketing Sales Analysis](Step-4-Results-and-Evaluation.png) 




![Marketing Sales Analysis](regression-plot.png) 








![Marketing Sales Analysis](Residual-distribution.png) 








![Marketing Sales Analysis](Q-Q-plot-of-residuals.png) 










![Marketing Sales Analysis](Scatterplot-of-residuals.png)  









## Step 5: Conclusion  

- **5.1 Key Takeaways**  
  - Data visualizations and exploratory data analysis are essential tools for determining whether linear regression is an appropriate method for modeling the relationship between two variables.  
  - A linear regression model provides insights into the relationship between two variables, allowing it to be expressed quantitatively.  

- **5.2 Framing Findings for Stakeholders**  
  - In the simple linear regression model:  
    - **Y-intercept:** 41.5326  
    - **Slope:** 8.1733  
  - Interpretation:  
    - A company that increases its radio promotion budget by **1 million dollars** could experience an **average sales increase of 8.1733 million dollars**.  
    - Companies spending **1 million dollars more** on radio promotions tend to generate **8.1733 million dollars more** in sales on average.  
  - **Statistical Significance:**  
    - The **p-value is 0.000**, which is much smaller than the common significance threshold of **0.05**.  
    - This indicates a **very low probability** that the observed results are due to random chance.  
  - **Hypothesis Testing:**  
    - **Null Hypothesis (H₀):** No relationship between radio promotion budget and sales (slope = 0).  
    - **Alternative Hypothesis (H₁):** A relationship exists (slope ≠ 0).  
    - The analysis allows us to **reject the null hypothesis**, confirming a relationship between radio promotion budget and sales.  
  - **Confidence Interval:**  
    - The **95% confidence interval** for the slope ranges from **7.791 to 8.555**, meaning there is a 95% probability that the true slope falls within this range.  

- **5.3 Framing the Findings for External Stakeholders**  
  - The analysis shows a **significant relationship** between **radio promotion budget and sales**.  
  - The **p-value of 0.000** and a **standard error of 0.194** support the validity of this finding.  
  - Specifically, a **1 million dollar increase in radio promotion budget** is associated with an **8.1733 million dollar increase in sales**, on average.  
  - These findings suggest that **investing in radio promotions can be an effective strategy for boosting sales**.  
  - However, **further analysis is recommended** to explore this relationship in different contexts, such as across industries or different product types.
 




 






## Step:6 Key Questions Answered  

During the analysis, I addressed several key questions to better understand the dataset and the linear regression model:  

### **1. Exploratory Data Analysis (EDA)**  
- **Q1:** What do you observe about the different variables included in the data?  
- **Q2:** What do you observe about the number of rows and columns in the dataset?  
- **Q3:** What do you observe about the number of rows containing missing values?  

### **2. Model Assumptions and Interpretation**  
- **Q4:** Is the assumption of linearity met?  
- **Q5:** What is the y-intercept?  
- **Q6:** What is the slope?  
- **Q7:** What is the linear equation expressing the relationship between sales and the radio promotion budget?  
- **Q8:** What does the slope mean in this context?  

### **3. Regression Results and Evaluation**  
- **Q9:** What do you observe from the regression plot?  
- **Q10:** What do you observe about the distribution of the residuals?  
- **Q11:** Is the assumption of normality met?  
- **Q12:** Are the assumptions of independent observation and homoscedasticity met?






## Connect with Me  

Autor: Gerard Nynkeu

- **GitHub:** [My GitHub Profile](https://github.com/gerardnynkeu) 
- **LinkedIn:** [My LinkedIn Profile](https://www.linkedin.com/in/gerard-nynkeu-njike-63282a327/)
























        


    




