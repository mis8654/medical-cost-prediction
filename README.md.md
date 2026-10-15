# Medical Cost Prediction using Machine Learning

A machine learning project that predicts a person's yearly medical insurance charges from age, sex, BMI, number of children, smoking status and region.

## Problem Statement
Healthcare costs differ widely from person to person, and insurers need a quick way to estimate them. This project uses machine learning to predict medical charges from a person's basic details.

## Dataset
Medical insurance dataset with 1,338 people and these columns: age, sex, bmi, children, smoker, region, charges.

## Tools Used
Python, Google Colab, pandas, numpy, matplotlib, seaborn, scikit-learn

## Method
1. Cleaned the data and converted text columns (sex, smoker, region) into numbers using one-hot encoding
2. Split the data: 80% for training and 20% for testing
3. Trained two models: Linear Regression and Random Forest
4. Compared the models using MAE, RMSE and R2 score

## Results

| Model | MAE ($) | RMSE ($) | R2 Score |
|---|---|---|---|
| Linear Regression | 4177 | 5956 | 0.807 |
| Random Forest | 2432 | 4253 | 0.902 |

Random Forest is the best model. It is off by about $2,400 on average and explains about 90% of the variation in medical charges. Smoking is the most important factor, followed by BMI and age.

## Graphs

![Charges distribution](https://raw.githubusercontent.com/mis8654/medical-cost-prediction/main/graph1_charges_distribution.png)

![Smoker vs charges](https://raw.githubusercontent.com/mis8654/medical-cost-prediction/main/graph2_smoker_vs_charges.png)

![Correlation heatmap](https://raw.githubusercontent.com/mis8654/medical-cost-prediction/main/graph3_correlation_heatmap.png)

![Actual vs predicted](https://raw.githubusercontent.com/mis8654/medical-cost-prediction/main/graph4_actual_vs_predicted.png)

## How to Run
1. Open [Google Colab](https://colab.research.google.com) and create a new notebook
2. Paste the code from the Python file in this repository into a cell
3. Click Run. The dataset downloads automatically

## Future Scope
- Try stronger models such as Gradient Boosting or XGBoost
- Train on a larger real-world dataset
- Deploy as a web app so anyone can enter details and get a prediction
