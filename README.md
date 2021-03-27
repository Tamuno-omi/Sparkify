# Sparkify
A blogpost for this project can be found here: [Predicting customer churn with PySpark](blank.com).


1. [Installation](#installation)
2. [Introduction](#introduction)
3. [Methodology](#methodology)
4. [File Descriptions](#file-descriptions)
5. [Licensing, Authors, Acknowledgements](#licensing-authors-acknowledgements)

## Installation
The code was developed using Python 3.6.3. Necessary packages beyond the Python Standard Library are:

* matplotlib==3.3.4
* numpy==1.19.5
* pandas==0.23.3
* pyspark==2.4.3
* seaborn==0.11.1 


## Introduction

Sparkify is a make belief music streaming app with free and paid tiers, users can upgrade, downgrade or cancel their service at any time, when users interact with the service they generate data, which can be used to gain insights, in this project we will be looking at identifying users who are at risk to churn i.e Cancelling their service altogether, the datasets used in this project was gotten from [Udacity](https://www.udacity.com/).

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

#### VI. Feature Importance.

#### VII. Conclusion

## File descriptions


## Licensing, Authors, Acknowledgements

This project was done as part of the [Udacity Data Scientist Nanodegree Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025).
