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

## Working with COVID-19 Dataset
(This section explains how the COVID-19 dataset is processed and analyzed.)

### Spread Measures
(Highlight the spread measures evaluated in the dataset.)

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
