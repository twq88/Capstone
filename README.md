# Capstone - Lending Club Capstone project


### Problem Statement

We are taking the position of an external credit risk consultancy providing services for Lending Club in December 2017. The company is facing litigation and share prices has just fallen sharply on the aftermath of a slew of scandals which shook investor confidence. Scandals include poor lending policies and excessive risk in the disbursement of loans to individuals. To implement more robust lending processes, this project looks at a standpoint from a consultant, advising Lending club on how it could have managed its credit risk by calculating RWA/credit scoring based on the IRB approach from the Basel 3 framework CRE35.

Credit scoring is a statistical model that combines several financial characteristics to evaluate a default risk of an enterprise by a single score to assess a customer creditworthiness. It works in a regulated framework: Basel II/III that is an internationally agreed set of measures developed by the Basel Committee on Banking Supervision regarding the capital requirements of banks, according to which banks must set aside proportional shares of capital, based on the risk assumed and evaluated by a rating tool.

1. Analyzing which top 5 features affect probability of default since this is the most crucial to the business.
2. Developing a model to predict this probability of default
3. Developing a model to predict the Exposure at default
4. Developing a model to predict the Loss given default


### Executive Summary

The dataset contains all available data for consumer loans issued from 2007 to 2015 by Lending Club: a large US peer-to-peer lending company. We have split this into 4 workbooks:

1. Data Cleaning and EDA- This notebook explores the consumer loans data of lending club where it then shows the data cleaning processes in conjunction with the exploratory data analysis being done on the data.
2. Modelling PD- In this workbook, we have used various types of machine learning models such as the logistic regression, random forest classifier well as the balanced bagging classifier. Logistic regression is used as a benchmark model since our dependent variable is a binary.
3. Modelling LGD- We will use the Linear Regression,Random Forest and AdaBoost,GradientBosst models with hyper parameter Gridsearch to find the best model to predict our recovery rate (recoveries/ funded amount). Random Forest model yielded the best  score of 98% 

4. Modelling EAD- We will use the Linear Regression,Random Forest and AdaBoost,GradientBosst models with hyper parameter Gridsearch to find the best model to predict credit conversion rate(ratio of the difference of the amount used at the moment of default to the total funded amount). EAD is then obtained by multiplying CCF with undrawn amount. Neural Networks yielded the best score 99%


### Conclusions and Recommendations


1. The best machine learning models include ensemble models such as random forests as Neural Network models. Now that we have the 3 components obtained, we will be able to obtain the EL by multiplying in formula PD X LDG X EAD. 

2. Research papers on these subjects might have recommended these models usage for specific component calculations. However, the limitations of these models and effectiveness are well documented. Given more time and processing power, I would look to improve models by adding hyperparameters during gridsearch and also try other dimensions reduction methods. Most research papers cite models with each component to be highly sensitive to a certain number of features
3. The top 5 features that affects probability of default are the following:
- Interest rates
- Loan repayment in Installment
- Loan amount
- Term of loan
- Debt to income ratio


### Data

Data sources:

PD
https://www.moodysanalytics.com/risk-perspectives-magazine/managing-disruption/spotlight/machine-learning-challenges-lessons-and-opportunities-in-credit-risk-modeling

LGD
FULLTEXT01.pdf (diva-portal.org)

SMOTE
 https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/ 

EAD/PD
Finalyse: Machine Learning in Risk Management
Sun-EnsembleLearningCreditRiskModeling-Oct2014.pdf (sas.com)
