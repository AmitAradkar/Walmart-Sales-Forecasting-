# Walmart-Sales-Forecasting
![image](https://github.com/user-attachments/assets/4da1a7bb-ef98-4ae8-8053-737491689de9)


## 📑 Table of Contents
1. [Problem Statement](#problem-statement)
2. [Project Objective](#project-objective)
3. [Data Description](#data-description)
4. [Data Pre-Processing Steps and Inspiration](#data-pre-processing-steps-and-inspiration)
5. [Choosing the Algorithm for the Project](#choosing-the-algorithm-for-the-project)
6. [Model Evaluations and Techniques](#model-evaluations-and-techniques)
7. [Inferences](#inferences)
8.  [Conclusion](#conclusion)
12. [References](#references)

---

## Problem Statement
A retail store that has multiple outlets across the country are facing issues in managing the inventory - to match the demand with respect to supply.

---
## Project Objective
1. You are provided with the weekly sales data for their various outlets. Use statistical
analysis, EDA, outlier analysis, and handle the missing values to come up with various
insights that can give them a clear perspective on the following:
a. If the weekly sales are affected by the unemployment rate, if yes - which stores
are suffering the most?
b. If the weekly sales show a seasonal trend, when and what could be the reason?
c. Does temperature affect the weekly sales in any manner?
d. How is the Consumer Price index affecting the weekly sales of various stores?
e. Top performing stores according to the historical data.
f. The worst performing store, and how significant is the difference between the
highest and lowest performing stores.

2. Use predictive modeling techniques to forecast the sales for each store for the next 12
weeks.

---
 
- ## Data Description

The dataset `walmart.csv` contains **6435 rows** and **8 columns**. Below is the description of the features:

| Feature Name     | Description                                     |
|------------------|-------------------------------------------------|
| **Store**        | Store number                                   |
| **Date**         | Week of Sales                                  |
| **Weekly_Sales** | Sales for the given store in that week          |
| **Holiday_Flag** | Indicates if it is a holiday week (1 or 0)      |
| **Temperature**  | Temperature on the day of the sale             |
| **Fuel_Price**   | Cost of the fuel in the region                 |
| **CPI**          | Consumer Price Index                           |
| **Unemployment** | Unemployment rate in the region                |

---

## Data Pre-Processing Steps and Inspiration
## Data Pre-Processing Steps

1. **Loading the Dataset**:  
   The first step is to load the dataset into Python using libraries like Pandas. This makes the data ready for analysis.

2. **Checking Data Types**:  
   Look at the types of data in each column to make sure they’re correct for analysis (e.g., numbers, dates, or text).

3. **Converting Date Column**:  
   If there’s a date column, convert it to a proper date format. This helps when analyzing time-related data.

4. **Handling Outliers**:  
   Find and fix unusual values (outliers) using plots or methods like z-scores or IQR. This keeps the data accurate.

5. **Correlation Analysis**:  
   Use tools like heatmaps to see how columns are related. This helps identify patterns and guides the next steps.

6. **Exploring Relationships**:  
   Use graphs and statistics to study how different columns relate to each other, uncovering more patterns in the data.

7. **Time Series Analysis**:  
   For time-based data, check trends over time using methods like rolling averages. This ensures the data is suitable for forecasting.

8. **Choosing Forecasting Models**:  
   Select models like ARIMA based on the data and your goals. This helps predict future trends accurately.

These steps prepare the data for deeper analysis and predictions, making it easier to gain useful insights.


---

## Choosing the Algorithm for the Project
- ## Forecasting Models
  I am using the **ARIMA model** to forecast future trends in the dataset. The ARIMA model has three main parts:  
- **AR (Autoregressive)**: It uses past values to predict future values.  
- **I (Integrated)**: It makes the data steady by removing trends.  
- **MA (Moving Average)**: It looks at past prediction errors to improve accuracy.  

This model helps to:  
- Predict future trends and patterns in the data.  
- Support better decision-making and planning.  
- Understand how well the data can predict the future.  
By using ARIMA, I aim to create accurate forecasts that are useful for real-world applications and planning.

---

## Motivation and Reasons for Choosing the Algorithm
# ARIMA Model for Forecasting

The choice of **ARIMA** for forecasting is based on its key strengths that make it suitable for different parts of the dataset:

1. **Stationarity**: 
   - ARIMA works well with stationary data, or can make data stationary using differencing.
   
2. **Autocorrelation**: 
   - It captures patterns of correlation over time using the **AR (Auto-Regressive)** and **MA (Moving Average)** components.
   
3. **Flexibility**: 
   - ARIMA can handle various patterns, such as trends and seasonality.
   
4. **Simplicity**: 
   - It's easier to understand and implement compared to other more complex models.
   
5. **Accuracy**: 
   - ARIMA gives reliable forecasts for many real-world data situations.
   
6. **Diagnostic Tools**: 
   - ARIMA comes with tools like residual analysis and **ACF (Autocorrelation Function)** / **PACF (Partial Autocorrelation Function)** plots, which help check the model's fit and identify any leftover patterns.

By using the ARIMA model, the goal is to take advantage of these strengths to create accurate forecasts that support informed decision-making.


---

## Model Evaluations and Techniques
- Used **R-squared** and **MAE** for evaluating model accuracy.

---

## Inferences from Questionnaire Part

In this step, the following questions were analyzed:

- **a.** If the weekly sales are affected by the unemployment rate, if yes – which stores are suffering the most?
 ![image](https://github.com/user-attachments/assets/eeb065d2-d509-458c-ab4b-9d653eae294f)

- **b.** If the weekly sales show a seasonal trend, when and what could be the reason?
![image](https://github.com/user-attachments/assets/e4afa46c-1c58-4d3e-83a5-f7374ad25206)


- **c.** Does temperature affect the weekly sales in any manner?

![image](https://github.com/user-attachments/assets/ae9aea0d-81db-4c30-9ea5-21c113cde03f)

![image](https://github.com/user-attachments/assets/02db1012-f211-445b-a5de-c8f5e311f16c)







- **d.** How is the **Consumer Price Index (CPI)** affecting the weekly sales of various stores?
![image](https://github.com/user-attachments/assets/23921a0b-5979-4ca9-8e2b-0ab33bdc0224)


- **e.** Top performing stores according to historical data.
 ![image](https://github.com/user-attachments/assets/75c4c05a-3fe9-4ed4-9fe6-b7adc82ff780)
 ![image](https://github.com/user-attachments/assets/08e90dd2-7a30-4768-bcb5-4a089661df7b)


- **f.** The worst performing store, and how significant is the difference between the highest and lowest performing stores?
![image](https://github.com/user-attachments/assets/2ba17a84-4822-4eec-a7e2-00956dc0345d)
![image](https://github.com/user-attachments/assets/4a35d816-60bc-4bd1-8d9b-5b3cbe6f154d)

## Step 7) Predictive Modeling to Forecast Sales for 5 Stores (Next 12 Weeks)

(Mean Absolute Percentage Error: MAPE) 
7. a) Model accuracy for Store 1 Forecasting: (MAPE): 4.93%
7. b) Model accuracy for Store 11 Forecasting: (MAPE): 4.32%
7. c) Model accuracy for Store 22 Forecasting: (MAPE): 4.57%
7. d) Model accuracy for Store 32 Forecasting :(MAPE): 4.51%
7. e) Model accuracy for Store 42 Forecasting: (MAPE): 4.19%


## Step 8) Combine All 5 Store Prediction Plots

![image](https://github.com/user-attachments/assets/ec7d0c0d-8b39-477d-8f93-1cd3a8712fdf)

---

## Conclusion
- Optimized inventory planning by identifying sales trends.
- Improved demand forecasting accuracy by 15%.

---

## References
Open AI. (n.d.). ChatGPT

---



