# Freight Delay Prediction

## Project Goal
The goal of this project is to analyze freight logistics data and build a predictive model that can identify shipments that are likely to be delayed. The project demonstrates how machine learning and data analysis can be applied to logistics operations to improve delivery reliability and operational planning.

## Problem Statement
Freight transportation is a critical part of supply chain operations, yet delivery delays frequently occur due to operational inefficiencies such as excessive idle time, long detention periods, or scheduling issues.

This project analyzes historical shipment data including trip details, delivery events, and operational metrics to understand the key factors contributing to delivery delays and to build models that predict delay risk.

## Dataset Overview
The project integrates multiple logistics datasets:

+ Loads dataset – shipment level information  
+ Trips dataset – trip performance metrics  
+ Delivery events dataset – scheduled and actual delivery timestamps  

These datasets are merged using **load_id** and **trip_id** to construct a comprehensive operational dataset.

## Tools & Technologies Used
+ Python  
+ Pandas  
+ NumPy  
+ Matplotlib  
+ Seaborn  
+ Scikit-learn  
+ Jupyter Notebook  

## Data Processing & Feature Engineering
Several features were engineered to improve analysis and predictive modeling:

Time-based features:
+ Scheduled hour  
+ Day of week  
+ Month  
+ Weekend indicator  

Operational features:
+ Revenue per mile  
+ Calculated fuel efficiency (MPG)  
+ Idle time ratio  
+ Distance buckets  
+ Detention time buckets  

The project also calculates **delivery delay hours** by comparing scheduled and actual delivery timestamps.

## Exploratory Data Analysis
EDA was conducted to understand patterns contributing to delivery delays, including:

+ Delay distribution across trips  
+ Delay probability by distance bucket  
+ Delay probability by idle time ratio  
+ Delay probability by detention time  
+ Correlation analysis between operational variables and delay time  

## Machine Learning Models
Two classification models were implemented to predict delayed deliveries.

### Logistic Regression
+ Features were scaled using **StandardScaler**  
+ Model trained to classify delayed vs on-time shipments  

### Random Forest Classifier
+ Used to capture nonlinear relationships between operational features and delays  
+ Feature importance analysis was conducted to identify the most influential predictors  

## Key Insights
The analysis revealed several operational patterns contributing to delays:

+ Higher **detention time** significantly increases the probability of delay  
+ Trips with higher **idle ratios** tend to experience operational inefficiencies  
+ Longer distance trips show varying delay patterns depending on operational factors  
+ Certain operational features strongly influence delay prediction  

## Operational Analytics Extensions
Additional analytical components were developed to simulate real-world logistics analytics systems.

### Route Risk Scoring
Routes were analyzed based on historical delay rates and categorized into:

+ Low Risk  
+ Medium Risk  
+ High Risk  

This allows logistics planners to identify routes with higher delay probability.

### Driver Performance Ranking
Driver performance was evaluated based on:

+ Number of trips completed  
+ Average delay rate  
+ Average idle time  

Drivers were ranked using a performance score to identify operational efficiency.

### Logistics KPI Dashboard
Key operational metrics were calculated and visualized:

+ Total number of trips  
+ Overall delay rate  
+ Average trip distance  
+ Average detention time  

These metrics help provide a quick overview of logistics system performance.

## Business Impact
The project demonstrates how predictive analytics can help logistics organizations proactively manage delivery operations. By identifying high-risk routes, inefficient driver patterns, and operational bottlenecks, companies can improve planning, reduce delays, and enhance overall supply chain efficiency.
