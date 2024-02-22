## Loan Status Prediction

Predict the loan to be approved or to be rejected for an applicant.

## About Dataset

In this Loan Status Prediction dataset, we have the data of applicants who previously applied for the loan based on the property which is a Property Loan. The bank will decide whether to give a loan to the applicant based on some factors such as Applicant Income, Loan Amount, previous Credit History, Co-applicant Income, etc… Our goal is to build a Machine Learning Model to predict the loan to be approved or to be rejected for an applicant.

## About the loan_data.csv file:

Loan_ID: A unique loan ID.
Gender: Either male or female.
Married: Weather Married(yes) or Not Marttied(No).
Dependents: Number of persons depending on the client.
Education: Applicant Education(Graduate or Undergraduate).
Self_Employed: Self-employed (Yes/No).
ApplicantIncome: Applicant income.
CoapplicantIncome: Co-applicant income.
LoanAmount: Loan amount in thousands.
Loan_Amount_Term: Terms of the loan in months.
Credit_History: Credit history meets guidelines.
Property_Area: Applicants are living either Urban, Semi-Urban or Rural.
Loan_Status: Loan approved (Y/N).
Goal:
In this project, we are going to classify an individual whether he/she can get the loan amount based on his/her Income, Education, Working Experience, Loan taken previously, and many more factors. Let’s get more into it by looking at the data.

## Environment Configuration (Installing virtual Env)

-pip install pipenv
-create a repo with your github account
-clone the repo in your working directory
-cd to the repo

## Installing Packages

-pipenv install jupyter notebook pandas numpy matplotlib seaborn scikit-learn pyarrow
Starting Virtual Env

## Starting Notebook

-pipenv shell
-jupyter-notebook

## Stoping Notebook

-Ctrl+c

## Deactiving Virtual Env

-exit

## Import libraries

-import numpy as np
-import pandas as pd
-import matplotlib.pyplot as plt
-import seaborn as sns
-from sklearn.model_selection import train_test_split
-from sklearn.feature_extraction import DictVectorizer
-from sklearn.linear_model import LogisticRegression
-from sklearn.metrics import accuracy_score

## Loading and Overviewing of Dataset

-df.head()
-df.tail().T
-df.info()
-df.shape()
-df.dtypes
-df.isnull().sum()
-unique instances()

## Data Preprocessing

- Normalize the column names to lower case
- Drop the ID column
- Remove the (+) sign on the Dependants column
- Fill the NaN in the (Dependants, Credit_History, Loan_Amount, Gender, Self_Employed) columns
- Replace categorical column(Loan-Status) with integers

## Exploratory Data Analysis (EDA)

-target variable analysis

## Data Preprocessing - Step 2

-Build a Validation Framework

## Feature Engineering

-Dividing our data into numerical and categorical
-perform the one-hot encoding
-convert the dataframe into dict
-DictVectorizer
-(fit) the train_dict

## Training The Model

-LogisticRegression
-compaire predicted truth vrs ground truth

The predictions of the model: a two-column matrix. The first column contains the probability that the target is zero (the application will be approved). The second column contains the opposite probability (the target is one, and the application will be rejected).
The output of the (probabilities) is often called soft predictions. These tell us the probability of rejection as a number between zero and one. It’s up to us to decide how to interpret this number and how to use it.

## Saving The Model

-import pickle
-specifyging where to save the file
-save the model

## Loading The Model

Load applicant Data to predict status (Approve/Reject) of application
