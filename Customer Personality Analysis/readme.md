# 🧠 Customer Personality Analysis

## 📌 Overview

This project dives into customer segmentation and behavior analysis using the **Marketing Campaign** dataset from Kaggle. The goal is to uncover patterns in demographics, lifestyle, and spending habits to help businesses design more personalized, targeted, and effective marketing strategies.

---

## 🎯 Project Objective

The objective is to:
- Explore and clean the dataset.
- Analyze customer demographics and behaviors.
- Segment customers into distinct clusters using unsupervised learning (K-Means).
- Provide actionable marketing recommendations based on customer segments.

---

## 📁 Dataset Overview

- **Source**: [Kaggle - Marketing Campaign Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
- **Rows**: 2240 customers
- **Columns**: 29 features, including:
  - Demographics: `Age`, `Income`, `Marital_Status`, `Education`
  - Behavior: `NumDealsPurchases`, `NumWebVisitsMonth`, `Complain`
  - Spending: Amounts spent on `Wine`, `Fruits`, `Meat`, etc.
  - Campaign data: Responses to different marketing campaigns

---

## 🧪 Project Workflow

### 1. 📥 Data Loading & Inspection
- Loaded and reviewed data structure
- Identified key variables and data types

### 2. 🧹 Data Cleaning & Preprocessing
- Handled missing values and outliers
- Converted data types and encoded categorical variables
- Created new features (e.g., total spending, age from birth year)

### 3. 📊 Exploratory Data Analysis (EDA)
- Demographic profiling
- Spending patterns visualization
- Correlation matrix analysis

### 4. 🔍 Customer Segmentation
- Feature selection for clustering
- Standardized variables
- Applied **K-Means Clustering** to identify customer groups
- Visualized clusters using PCA and Seaborn plots

### 5. 📈 Insights & Recommendations
- Summarized traits of each customer segment
- Suggested targeted marketing strategies per cluster

---

## 📌 Key Insights

- High-income customers tend to spend more on luxury goods like wine and meat.
- Younger customers are more active in online campaigns and web purchases.
- Middle-aged customers with children respond less to promotional campaigns.
- At least **4 distinct customer segments** were identified, each requiring different marketing approaches.

---

## 💡 Business Recommendations

- 🎯 **Cluster 1**: Young, single professionals — target with digital campaigns and online deals.
- 🍷 **Cluster 2**: High-income wine lovers — promote exclusive, premium products.
- 🧺 **Cluster 3**: Price-sensitive families — offer bundle deals and family discounts.
- 🔄 **Cluster 4**: Low-engagement customers — consider reactivation or loyalty programs.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**, **Plotly**
- **Scikit-learn** (K-Means, PCA)
- **Jupyter Notebook**

---

## 📂 Repository Structure

├── customer-personality-analysis.ipynb
├── README.md
└── dataset/
└── marketing_campaign.csv


---

## 👤 Author

**Gerard Nynkeu**  
Aspiring Data Analyst | Passionate about customer insights & business analytics

> 📫 Let’s connect on [LinkedIn](#)  
> ⭐ Feel free to star this repository if you found it useful!

---
