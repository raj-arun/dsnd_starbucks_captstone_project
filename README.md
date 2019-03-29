# Data Science Nano Degree Starbucks Captstone Project
Capstone Project as part of Data Science Nano Degree Program

# Project Overview

The Starbucks Udacity Data Scientist Nanodegree Capstone challenge data set is a simulation of customer behavior on the Starbucks rewards mobile application. Periodically, Starbucks sends offers to users that may be an advertisement, discount, or buy one get on free (BOGO). An important characteristic regarding this dataset is that not all users receive the same offer.

This data set contains three files. The first file describes the characteristics of each offer, including its duration and the amount a customer needs to spend to complete it (difficulty). The second file contains customer demographic data including their age, gender, income, and when they created an account on the Starbucks rewards mobile application. The third file describes customer purchases and when they received, viewed, and completed an offer. An offer is only successful when a customer both views an offer and meets or exceeds its difficulty within the offer's duration.

# Problem Statement / Metrics

The problem that I chose to solve was to build a model that, given a set of features predicts the chances of an offer being successful or not. My strategy for solving this problem involves four steps. 
  - First step is to clean up up the data sets
  - Second, I combined offer portfolio, customer profile, and transaction data into one data frame and this was the fun part. 
  - In the next step I perform more analysis of the dataset to check the following:
    - Correlation of Income to offer being successful
    - Who spens more money (Women or Men)
    - How reward affects the success of the offer
    - How difficutly affects the success of the offer
    - How duration affects the success of the offer
  - In the last step, create train and evaulate the the models' precision and recall. Parem
    - SVM
    - Logistic Regression
    - Ramdon Forest Classifer 
  - I will be using Confusion matrix to visualize the model performance
  - Grid Search will be used to find the best parameter values to further tune the models.
  
# Results Summary
Model ranking based on training data accuracy
  - RandomForestClassifier Model Accuracy: 0.738
  - LogisticRegression Model Accuracy: 0.725
  - SVM Model Accuracy: 0.722

Model ranking based on training data F1-score
  - RandomForestClassifier model f1-score: 0.74
  - LogisticRegression model f1-score: 0.73
  - SVM Model f1-score: .72

Results suggest that the random forest model has the best training data accuracy and F1-score

You can read more about this project in my medium blog [here](https://medium.com/@s.arun.raj/analyzing-starbucks-offers-data-set-a28993ee9c5e).

**Feature importance** refers to a numerical value that describes a feature's contribution to building a model that maximizes its evaluation metric. A random forest classifier is an example of a model that estimates feature importance during training. The below are the top features:

  - Offer difficulty (how much money a customer must spend to complete an offer)
  - Offer reward
  - Offer duration
  - Customer income
  - 2018 (Year when the user created the account)
  - social (whether the offers are available through social media) 
  - informational

For this project the most important steps are the data cleansing activities and combining the data sets into one data set. Feature engineering is very important aspect of any data science project and here is a [great article on the same](https://machinelearningmastery.com/discover-feature-engineering-how-to-engineer-features-and-how-to-get-good-at-it/).

# Files
Starbucks_Project.ipynb : Jupyter notebook that performs the below tasks:
  - Performs EDA on various data sets
  - Combines offer portfolio, customer demographic, and customer transaction data
  - Generates training customer demographic data visualizations and computes summary statistics
  - Generates logistic regression, random forest, & SVM models

LICENSE
  - Repository license file

README.md
  - Markdown file that summarizes this repository

# References
  - [Feature Engineering](https://machinelearningmastery.com/discover-feature-engineering-how-to-engineer-features-and-how-to-get-good-at-it/)  
  - [Grid Search vs Random Search](https://scikit-learn.org/stable/auto_examples/model_selection/plot_randomized_search.html)  
  - [sklearn Random Forest Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)  
  - [Random Forest Blog](https://medium.com/machine-learning-101/chapter-5-random-forest-classifier-56dc7425c3e1)  
  - [Blog on Logistic Regression](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc)
  - [Miltilabel Binarizer](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MultiLabelBinarizer.html#sklearn.preprocessing.MultiLabelBinarizer)
  - [Using iloc, loc, & ix in Pandas](https://www.shanelynn.ie/select-pandas-dataframe-rows-and-columns-using-iloc-loc-and-ix/)
