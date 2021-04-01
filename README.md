# Sparkify
A blogpost for this project can be found here: [Predicting customer churn with PySpark](https://tamuno-omi.medium.com/predicting-user-churn-with-pyspark-8e925248759).


1. [Installation](#installation)
2. [Overview](#overview)
3. [Methodology](#methodology)
4. [Licensing, Authors, Acknowledgements](#licensing-authors-acknowledgements)

## Installation
The code was developed using Python 3.6.3. Necessary packages beyond the Python Standard Library are:

* matplotlib==3.3.4
* numpy==1.19.5
* pandas==0.23.3
* pyspark==2.4.3
* seaborn==0.11.1 


## Overview

Sparkify is a make belief music streaming app with free and paid tiers, users can upgrade, downgrade or cancel their service at any time, when users interact with the service they generate data, which can be used to gain insights, in this project we will be looking at identifying users who are at risk to churn (users who cancel their service) the datasets used in this project was gotten from [Udacity](https://www.udacity.com/).

## Metrics for Model Performance:

We select F-1 score as our evaluation metrics. The reason we use F-1 score here is because it gives us a simple measure of the precision (whether we send offer to the right person) and recall (whether we miss one that we should’ve sent the offer) of the model. We want to identify those who are likely to churn and give them some special offers in trying to keep the customer, but at the same time, we do not want to send too many offers (most likely a monetary incentive) to those who are not as likely to churn and therefore wasting money and resources.

## Methodology 

The project is divided into the following sections
#### I. A Look at the data
In the section we wrangle the data by performing cleaning and transforming tasks.

#### II. Exploratory Data Analysis
Here I explored the dataset provided for the project to gain a better understanding about the data and finally churn was defined by the cancellation confirmation page.

#### III. Feature Engineering
After familiarizing ourselves with the data we select promising featues to build our model.

#### IV. Modelling.
Logistic Regression, Gradient Boosted Trees, Random Forest classifiers were used

#### V. Evaluation.

| **Classification Model** | **Accuracy** | **F1-Score** | **Time(s)** |
|--------------------------|--------------|--------------|-------------|
| Logistic Regression      | 0.88         | 0.83         | 378.90      |
| Gradient Boosted Trees   | 0.65         | 0.69         | 849.36      |
| Support Vector Machine   | 0.88         | 0.83         | 477.02      |
| Random Forest            | 0.88         | 0.83         | 400.06      |

The **Random Forest Model** was selected as the Final Model because of its accuracy , we conducted a grid search to fine tune our model this time. In the future, we may instead implement Logistic Regression for more time efficiency. our model this time and reached **83.91% accuracy and a F1 score of 0.77** It is interesting to note we cannot outperform the accuracy and F1 score obtained with default parameters, probably due to the small size of the dataset.

#### VI. Feature Importance.
We utilized the feature importance attribute of the Random Forest model and we observed that the length of using the service plays a very important role.


![image](https://user-images.githubusercontent.com/39832553/113281035-fc66fb80-92dc-11eb-9ed4-550b35a375bd.png)

#### VII. Conclusion
We implemented a model to predict customer churn on a music streaming sevice, after loading the data we performed cleaning tasks removing rows without user id, generated additional columns from exiting one e.g converting timestamp to get date, year, month, weekday, number of days since registration, after that we defined churn using the 'cancellation confirmation' page and explored its relationship to other variable, after which we selected features we found interesting to implement in out model, we selected the logistic regression, GBM, SVM, and RF classification models and selected the Random Forest as our final model for predicting our result.

Reflection The project gave me an opportunity to work with a larger volume of data than I would have on a personal laptop, and also gave me a highlevel exposure to the Apache spark and IBM WATSON STUDIO enviroment

**Improvement**
The features can be improved a lot after considering more factors, adding more domain knowledges and expertise. Although the volume of data may required tools such as spark to analyze, but we can use more data to have better results as the user base grow, the model has a huge potential to improve if the sample size increase, and the expected performance will also increase. The classification models could be further improved in the hyperparameter tuning process with extended parameter grids to search a broader range of possible parameter combinations.

## Licensing, Authors, Acknowledgements

This project was done as part of the [Udacity Data Scientist Nanodegree Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025).
