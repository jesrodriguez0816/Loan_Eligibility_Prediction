# Phase 5: Loan Eligibility Analysis

## Jessica Rodriguez
## Flatiron School
## Github: jesrodriguez0816

### Overview

The goal of this project was to build a binary classifier to predict whether or not a customer would default on a loan.

The following questions were addressed:

* What features are the primary determinants of risk?
* Are there any predictable patterns?
* How could stakeholders benefit from these findings?

It is in the best interest of any company to better understand the behaviors of their consumers. This project offers insights to help a lending organization understand the predictive factors that contribute to a borrower defaulting on thier loan. 

### About the Data

The dataset (sourced on [Kaggle](https://www.kaggle.com/datasets/subhamjain/loan-prediction-based-on-customer-behavior/code?select=Training+Data.csv)) contains the behavioral information of more than 25,000 loan borrowers. It includes the following 12 columns:

* **income*
* **age**
* **experience**
* **married**
* **house_ownership**
* **car_ownership**
* **risk_flag**
* **currentjobyears**
* **currenthouseyears**
* **city**
* **state**

The **"risk_flag"** column indicates whether there has been a past loan default. When building the classifier, this was our target variable.

### Process

The [CRISPDM](https://www.datascience-pm.com/crisp-dm-2/) data science process was used, which includes the following 6 phases: 
1. Business understanding – What does the business need?

2. Data understanding – What data do we have / need? Is it clean?

3. Data preparation – How do we organize the data for modeling?

4. Modeling – What modeling techniques should we apply?

5. Evaluation – Which model best meets the business objectives?

6. Deployment – How do stakeholders access the results?

### Best Metric

Because classes in this dataset are imbalanced, accuracty was not used at a metric. An accuracy score would have the potential to be high and misleading. Insterad, the precision/recall score and F1 score were considered.

In statistics, a type I error is a false-positive result, meaning that a null hypothesis is rejected when it is actually true. A type II error is a false-negative result, meaning that a null hypothesis is not rejected when it is actually false.

For this project, incorrectly classifying a false-negative (type II error) would be worse than incorrectly classifying a false-positive. A false negative would mean that the reality of a customer defaulting on thier loan would be overlooked.

The overall goal of this project was to **minimize false-negative results**.

### Building a Classifier

The following models were built and evaluated for recall:
* Logistic Regression
* K-Nearest Neightbors
* Decision Tree
* Random Forest
* Bagged Trees + Decision Tree
* AdaBoost
* Gradient Boost
* XGBoost

### Visualizing Results of the Model using SHAP

SHAPley Additive exPlanations is a tool that creates visualizations for a machine learning model. The resource I used to fit SHAP to my data can be found HERE.

On the right side of the graph below, the legend indicates that RED is HIGH feature value and BLUE is LOW feature value. On the y axis, the features are divided individually. The x axis ranks how significant the impact is.

### Findings and Reccomendation

# Get random sample of data
df = df.sample(frac=1)

