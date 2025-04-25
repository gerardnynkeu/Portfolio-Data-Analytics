# COVID-19 Global Happiness Analysis with Python

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Overview](#dataset-overview)
3. [Import Modules](#import-modules)
4. [Working with COVID-19 Dataset](#working-with-covid-19-dataset)
   - [Spread Measures](#spread-measures)
5. [World Happiness Report](#world-happiness-report)
6. [Visualizations](#visualizations)
7. [Conclusions & Key Findings](#conclusions--key-findings)
8. [Business Insights & Recommendations](#business-insights--recommendations)
9. [Tools & Technologies](#tools--technologies)
10. [References](#references)
11. [Contact](#contact)

---

## Introduction

This project aims to explore the global impact of COVID-19 and how it correlates with various socio-economic indicators. By analyzing the confirmed COVID-19 cases across different countries and comparing them with metrics from the World Happiness Report, the project provides insights into how countries with different levels of development and well-being managed the spread of the virus.

We investigate:

    How fast and wide COVID-19 spread in different regions.

    The maximum infection rates per country.

    The relationship between the pandemic's impact and factors like GDP per capita, social support, healthy life expectancy, and freedom to make life choices.

The analysis leverages Python’s robust data science stack to clean, merge, analyze, and visualize real-world datasets.

## Dataset Overview

1. COVID-19 Confirmed Cases Dataset

    File: covid19_Confirmed_dataset.csv

    Source: Johns Hopkins University (Time-series COVID-19 data)

    Description: This dataset contains daily confirmed COVID-19 cases for each region globally. The data spans from January 22, 2020, to April 30, 2020, and includes:

        Province/State

        Country/Region

        Lat and Long

        A timeline of confirmed cases (one column per date)

Preprocessing included:

    Dropping latitude and longitude columns.

    Aggregating data by Country/Region.

    Calculating the first derivative of cases (daily increases).

    Identifying the maximum infection rate per country.

2. World Happiness Report Dataset

    File: worldwide_happiness_report.csv

    Source: 2019 World Happiness Report

    Description: Contains socio-economic indicators for over 150 countries. Key columns used in this analysis include:

        Country or region

        GDP per capita

        Social support

        Healthy life expectancy

        Freedom to make life choices

Preprocessing included:

    Dropping less relevant columns such as Overall rank, Generosity, and Perceptions of corruption.

    Cleaning column names and setting the index to Country or region.



## Import Modules

(List and explain the Python libraries and modules utilized in the project.) 


![Import Modules](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/COVID-19-Global-Happiness-Analysis-with-Python/import%20module.png?raw=true)

## Working with COVID-19 Dataset
(This section explains how the COVID-19 dataset is processed and analyzed.) 


In this step, we load and preprocess the global COVID-19 confirmed cases dataset. The data is initially structured by province/state and date, and includes latitude and longitude, which are not needed for our analysis and are removed.

Key actions performed:

    ✅ Loaded the time-series data from Kaggle.

    🧹 Cleaned the dataset by dropping geolocation columns.

    📊 Aggregated case numbers by Country/Region to simplify the analysis.

    🔢 Converted all values to numeric types for accurate computation.

    📈 Visualized the progression of COVID-19 in China, Italy, and Spain over time to observe early global patterns and compare trends. 


![Visualization 1](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/COVID-19-Global-Happiness-Analysis-with-Python/viz1.png?raw=true) 


**COVID-19 Case Growth Comparison: China, Italy, and Spain (Jan–Apr 2020)**

This line chart visualizes the cumulative number of confirmed COVID-19 cases in China, Italy, and Spain from late January to April 2020. Initially, China experienced a rapid increase in cases, peaking early before stabilizing. In contrast, Italy and Spain showed a delayed but much steeper rise, eventually surpassing China in total reported cases. The visualization highlights how the pandemic unfolded differently across countries, emphasizing the critical timing and intensity of outbreaks in Europe compared to the earlier wave in China. The data underscores the global variability in outbreak trajectories and healthcare responses.


### Spread Measures

we need to find a good measure reperestend as a number, describing the spread of the virus in a country. 

![Spread Measure](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/COVID-19-Global-Happiness-Analysis-with-Python/spread%20measure.png?raw=true) 

**Spread Measure Line Chart**

This plot shows how a numerical value (such as stock prices, sales, or measurements) evolves over three consecutive dates. The upward trend indicates a consistent increase, with a sharper rise between the second and third points. The x-axis represents dates, and the y-axis represents the measured values. The graph was created using Python's Matplotlib library.


![Visualization 2](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/COVID-19-Global-Happiness-Analysis-with-Python/viz2.png?raw=true) 


**Daily New COVID-19 Cases in China (Jan–Apr 2020)**

This chart illustrates the daily number of new confirmed COVID-19 cases in China during the early phase of the pandemic. The data reveals a rapid rise in cases peaking dramatically around mid-February, followed by a sharp decline. The large spike is likely associated with a change in case reporting methodology. After the peak, new daily cases remained consistently low, reflecting the effectiveness of strict containment and mitigation measures implemented by Chinese authorities. This visualization showcases the impact of aggressive public health interventions in controlling an outbreak's spread.


![China Visualization](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/COVID-19-Global-Happiness-Analysis-with-Python/china.png?raw=true) 


**Maximum Daily Infection Rates: China, Italy, and Spain**

This analysis identifies the highest single-day increase in confirmed COVID-19 cases for three countries using the .diff().max() method on the time series data. China reported the highest daily spike with 15,136 cases, likely reflecting a change in diagnostic criteria. Spain followed with a peak of 9,630 cases, and Italy with 6,557 cases. These figures highlight the varying outbreak intensities and reporting patterns across countries, offering insight into how the pandemic unfolded differently in each region.



## World Happiness Report
(Discuss how the World Happiness Report is analyzed in the project.)

## Visualizations
(Include key visualizations and explain their significance.)

## Conclusions & Key Findings
(Summarize the insights and findings from the analysis.)

## Business Insights & Recommendations
(Provide actionable insights and recommendations based on the findings.)

## Tools & Technologies
- **Programming Language**: Python
- **Libraries Used**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Others**: Jupyter Notebook

## References
(Include references to data sources, documentation, and other materials.)

## Contact
Feel free to reach out for further information:

- **Author**: Gerard Nynkeu  
- **LinkedIn**: [https://www.linkedin.com/in/gerard-nynkeu-njike-63282a327/](https://www.linkedin.com/in/gerard-nynkeu-njike-63282a327/)  
- **GitHub**: [gerardnynkeu](https://github.com/gerardnynkeu)  
- **Email**: [gerardnynkeu@yahoo.de](mailto:gerardnynkeu@yahoo.de)
