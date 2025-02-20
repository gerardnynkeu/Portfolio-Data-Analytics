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
 
- [Step 6:Key Questions Answered](#step-6-Key-Questions-Answered)



  

  
 



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








🔗 Pairwise Relationships

In this step, I explore the pairwise relationships between different variables in the dataset to identify correlations and potential patterns. This helps me understand how variables interact with each other before building the regression model.

I typically use a pairplot (scatterplot matrix) to visualize these relationships:

    If two variables show a linear pattern, they are likely correlated, which is useful for regression modeling.
    If the points form a random cloud, there may be little or no correlation between them.
    If the relationship appears non-linear, a different modeling approach may be required.

By analyzing pairwise relationships, I ensure that I select the most relevant variables for my model and check for potential multicollinearity issues. 🚀








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









📈 Regression Plot

In this step, I visualize the relationship between the independent variable and the dependent variable using a regression plot. This helps me assess how well the linear regression model fits the data.

The regression plot includes:

    A scatterplot of actual data points, showing the relationship between the variables.
    A best-fit regression line, which represents the predicted values from my model.
    A confidence interval, indicating the uncertainty around the regression line.

Key Observations:

    If the data points are closely aligned with the regression line, this suggests a strong linear relationship.
    If the points are widely scattered, this may indicate weak correlation or the need for a more complex model.



    
    


![Marketing Sales Analysis](regression-plot.png) 







📊 Residual Distribution

In this step, I analyze the distribution of residuals to check whether they follow a normal distribution, which is a key assumption in linear regression.

I visualize the residuals using a histogram or density plot to observe their shape:

    If the residuals form a bell-shaped curve, this indicates normality, meaning my model's predictions are unbiased.
    If the distribution is skewed or has multiple peaks, this suggests that the model may be missing important patterns in the data.
    If the residuals have extreme outliers, they might indicate the presence of influential data points affecting the regression results.

By examining the residual distribution, I ensure that my regression model produces reliable predictions and meets the normality assumption. 🚀 







![Marketing Sales Analysis](Residual-distribution.png) 










📊 Q-Q Plot of Residuals

In this step, I use the Q-Q (Quantile-Quantile) plot to check whether the residuals follow a normal distribution, which is a key assumption of linear regression.

The Q-Q plot compares the quantiles of the residuals with the quantiles of a standard normal distribution:

    If the points fall along a straight diagonal line, the residuals are normally distributed, meaning the assumption of normality is satisfied.
    If the points deviate significantly from the line, especially at the ends, this indicates skewness or heavy tails, suggesting that the residuals are not normally distributed.

By analyzing the Q-Q plot, I verify whether my model meets the normality assumption, ensuring reliable statistical inferences from the regression results. 🚀 











![Marketing Sales Analysis](Q-Q-plot-of-residuals.png) 














📉 Scatterplot of Residuals

In this step, I analyze the scatterplot of residuals to check if the assumptions of homoscedasticity and independent errors are met.

Residuals represent the difference between the actual and predicted values. A well-fitted linear regression model should have residuals randomly scattered around zero without any clear pattern.

    If the residuals show no pattern and are evenly distributed, this confirms homoscedasticity (constant variance).
    If a funnel shape or systematic trend appears, this suggests heteroscedasticity, meaning the variance of residuals changes across different values.
    Any clustering or autocorrelation might indicate that independent observations assumption is violated.

By examining this plot, I ensure that my model is not biased and that the linear regression assumptions hold. 🚀 







![Marketing Sales Analysis](Scatterplot-of-residuals.png)  









## Step:5 Key Questions Answered  

During the analysis, I addressed several key questions to better understand the dataset and the linear regression model:  

### **1. Exploratory Data Analysis (EDA)**  
- **Q1:** What do you observe about the different variables included in the data?   
The dataset includes: TV promotion budget categorized as "Low," "Medium," or "High." Budgets for radio and social media promotions. Influencer type ("Mega," "Macro," "Micro," or "Nano") based on follower count. Sales generated from the promotion. 

- **Q2:** What do you observe about the number of rows and columns in the dataset? 
The dataset contains 572 rows and 5 columns, representing 572 companies and details on their promotion strategies and resulting sales.

- **Q3:** What do you observe about the number of rows containing missing values? 
Three rows have missing values, a small proportion of the dataset. These rows can be removed to prepare the data for modeling.

### **2. Model Assumptions and Interpretation**  
- **Q4:** Is the assumption of linearity met?
The scatter plot of Sales versus Radio shows the points forming a pattern that aligns closely with a straight line, indicating a positive relationship between the two variables. This suggests that the assumption of linearity is likely satisfied.

- **Q5:** What is the y-intercept?
The y-intercept is 41.5326.

- **Q6:** What is the slope?
The slope is 8.1733.
 
- **Q7:** What is the linear equation expressing the relationship between sales and the radio promotion budget?
 y= slope × 𝑥 + y-intercept y=slope×x+y-intercept? The equation is: sales 8.1733 × radio promotion budget + 41.5326 sales=8.1733×radio promotion budget+41.5326

- **Q8:** What does the slope mean in this context?
One interpretation: For every additional 1 million dollars invested in the radio promotion budget, the company's sales increase by 8.1733 million dollars on average. Another interpretation: Companies that allocate 1 million dollars more to their radio promotion budget typically achieve an additional 8.1733 million dollars in sales on average.

### **3. Regression Results and Evaluation**  
- **Q9:** What do you observe from the regression plot?
The regression plot shows a roughly linear relationship between the two variables, with the best fit line indicating this trend. This supports the assumption of linearity.

- **Q10:** What do you observe about the distribution of the residuals?
Question 10: What do you observe about the distribution of the residuals in the preceding visualization?
The residuals appear to follow an approximately normal distribution, suggesting that the assumption of normality is likely satisfied.

- **Q11:** Is the assumption of normality met?
In the Q-Q plot, the points align closely with the upward-trending diagonal line. This indicates that the assumption of normality is satisfied.

- **Q12:** Are the assumptions of independent observation and homoscedasticity met?
In the scatterplot, the data points resemble a random cloud without any clear pattern, suggesting that the assumption of independent observations is likely upheld. Additionally, since the residuals seem to be evenly distributed, the assumption of homoscedasticity also appears to be satisfied.




## Step 6: Conclusion  

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
 
  
 


## 7. Tools & Technologies

### Programming Language:
- Python 🐍

### Data Manipulation & Analysis:
- Pandas 📊
- NumPy 🔢

### Data Visualization:
- Matplotlib 📈
- Seaborn 🎨
- Plotly 📊 (optional for interactive plots)

### Machine Learning (if applicable):
- Scikit-learn 🤖
- Statsmodels 📊 (for regression analysis)

### Data Preprocessing:
- Scikit-learn (for scaling & encoding)
- Pandas (for handling missing values & transformations)

### Notebook Environment:
- Jupyter Notebook 📓
- Google Colab (if working in the cloud) ☁️

### Version Control:
- Git & GitHub 📝

### Deployment (if needed):
- Streamlit 🚀 (for building interactive dashboards)
- Flask/Django (for API development)




## 8. Limitations

1. **Data Quality Issues**  
   - Some missing values in the dataset (e.g., "TV" and "Sales" have 571 non-null values instead of 572).  
   - "TV" and "Influencer" are categorical but stored as objects, which may require preprocessing.

2. **Limited Feature Set**  
   - The dataset includes only a few marketing channels. Other factors like seasonality, competitor activities, or economic conditions are not considered.  

3. **Correlation vs Causation**  
   - Regression analysis can identify relationships but does not prove causality. External factors might influence sales.  

4. **Categorical Variable Encoding**  
   - "TV" and "Influencer" categories might require proper encoding (e.g., one-hot encoding, ordinal encoding) for better model performance.  

5. **Potential Non-Linearity**  
   - A simple linear regression model may not capture complex interactions between marketing channels. Advanced techniques (e.g., polynomial regression, decision trees) might improve predictions.  

6. **Small Sample Size**  
   - With only 572 data points, the model might not generalize well to real-world scenarios with larger datasets.
  





## 9. References

1. **Pandas Documentation** - Data manipulation and analysis  
   - [https://pandas.pydata.org/docs/](https://pandas.pydata.org/docs/)  

2. **NumPy Documentation** - Numerical computing  
   - [https://numpy.org/doc/](https://numpy.org/doc/)  

3. **Matplotlib & Seaborn Documentation** - Data visualization  
   - Matplotlib: [https://matplotlib.org/stable/contents.html](https://matplotlib.org/stable/contents.html)  
   - Seaborn: [https://seaborn.pydata.org/](https://seaborn.pydata.org/)  

4. **Scikit-learn Documentation** - Machine learning & regression  
   - [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html)  

5. **Statsmodels Documentation** - Statistical modeling & regression analysis  
   - [https://www.statsmodels.org/stable/index.html](https://www.statsmodels.org/stable/index.html)  

6. **Marketing Analytics Concepts**  
   - "Marketing Analytics: Data-Driven Techniques with Microsoft Excel" by Wayne L. Winston  
   - "Marketing Data Science" by Thomas W. Miller  

7. **Kaggle Datasets & Competitions** - Explore similar datasets  
   - [https://www.kaggle.com/datasets](https://www.kaggle.com/datasets)  
   - [https://www.kaggle.com/competitions](https://www.kaggle.com/competitions)  





## Connect with Me  

Autor: Gerard Nynkeu

- **GitHub:** [My GitHub Profile](https://github.com/gerardnynkeu) 
- **LinkedIn:** [My LinkedIn Profile](https://www.linkedin.com/in/gerard-nynkeu-njike-63282a327/)
























        


    




