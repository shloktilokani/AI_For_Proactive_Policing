# AI For Proactive Policing Analysis

![Preview](res/Recording%202025-06-12%20132132.gif)

## Overview

This project focuses on analyzing historical crime data to identify patterns, predict future crime occurrences, and enable proactive policing strategies using Artificial Intelligence. The goal is to assist law enforcement agencies and policymakers in making informed decisions for crime reduction and public safety enhancement by optimizing resource allocation and implementing targeted interventions.

## Dataset

The analysis utilizes a crime dataset for India, which includes various attributes related to reported incidents. Key features in the dataset include:

- `Report Number`: Unique identifier for each crime report.
- `Date Reported`: Date when the crime was reported.
- `Date of Occurrence`: Date when the crime occurred.
- `Time of Occurrence`: Time when the crime occurred.
- `City`: City where the crime took place.
- `Crime Code`: Numerical code for the type of crime.
- `Crime Description`: Detailed description of the crime.
- `Victim Age`: Age of the victim.
- `Victim Gender`: Gender of the victim.
- `Weapon Used`: Type of weapon used (if any).
- `Crime Domain`: Categorization of the crime.
- `Police Deployed`: Number of police deployed for the incident.
- `Case Closed`: Status of the case (closed or open).

### Download Dataset

You can find the dataset used in this analysis on Kaggle:
[Indian Crimes Dataset](https://www.kaggle.com/datasets/sudhanvahg/indian-crimes-dataset)

## Methodology

1. **Data Loading and Initial Exploration**
    - The dataset is loaded using `pandas`.
    - Initial inspection (`df.info()`, `df.head()`, `df.describe()`) is performed to understand its structure, data types, and summary statistics.

2. **Data Preprocessing**
    - Date and time columns (`Date Reported`, `Date of Occurrence`, `Time of Occurrence`) are converted to appropriate datetime formats for time-series analysis.
    - Missing values, particularly in `Weapon Used`, are identified and handled (e.g., through imputation or by noting their presence).
    - Feature engineering might be applied to extract additional insights (e.g., hour of day, day of week).

3. **Exploratory Data Analysis (EDA)**
    - Visualizations using `matplotlib` and `seaborn` are generated to explore crime trends over time, crime distribution by city, common crime types, and victim demographics.
    - Insights into high-risk areas and peak crime times are derived.

4. **Time Series Analysis and Predictive Modeling**
    - Time series models, such as ARIMA (Autoregressive Integrated Moving Average), are applied to forecast future crime trends based on historical patterns.
    - The project aims to identify future crime hotspots and potential increases in specific crime types.

5. **Insights and Conclusions**
    - Based on descriptive, diagnostic, and predictive analyses, key insights are drawn regarding crime patterns and potential future risks.
    - Conclusions highlight the importance of a multi-faceted approach to crime analysis, emphasizing data-driven decision-making, targeted interventions, continuous monitoring, and community engagement.

## Results

- The analysis identifies significant crime trends and patterns within the Indian dataset.
- Predictive models, including ARIMA, provide forecasts for future crime rates, aiding in proactive resource allocation.
- Visualizations illustrate crime distribution across different cities and over various time periods, highlighting high-risk zones and times.
- The findings support the development of informed strategies for crime prevention, such as allocating resources to high-crime areas during peak times to mitigate risks, and guiding policymaking and proactive crime prevention strategies.

## Dependencies

The project requires the following Python libraries:

```bash
pip install pandas numpy matplotlib seaborn statsmodels
