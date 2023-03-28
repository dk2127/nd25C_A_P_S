# Udacity Capstone Project - Starbucks Offer Analytics

# Introduction / Overview


We will leverage what we’ve learned throughout the program to build a data science project, for Starbucks Offer Analytics.


We have datasets containing simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer, and that is the challenge to solve with this data set. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

## Objective

Our objective is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. 


# Steps

We will be following steps of the data science process:

- First we will define the problem we want to solve and investigate potential solutions.
- Next, we will perform analysis through visualizations and data exploration to have a better understanding of what algorithms and features are appropriate for solving the problem.
- We  will then implement the algorithms/models and metrics, documenting the preprocessing, refinement, and post-processing steps along the way.
- Afterward, we will collect results about our findings, visualize significant quantities, validate/justify our results, and make any concluding remarks about whether our implementation adequately solves the problem.
- We will construct a Capstone Project Report as a blog post to document all of the steps from start to finish of our project and provide link at the bottom of this page.


# Installation
   
This project was created and run using Python version 3.9.12.
The notebook contained in this repository should be at main level. The data files will need to be in the **data** subdirectory.

## Libraries used

Most of the libraries used for this project are open source, readily available online: 

- pandas
- pandas.plotting |- scatter_matrix

- numpy 
- math
- json
- datetime |- datetime
- scipy.stats 

- sklearn.metrics |- confusion_matrix, silhouette_score, calinski_harabasz_score, davies_bouldin_score
- sklearn.metrics |- classification_report, accuracy_score, ConfusionMatrixDisplay, mean_squared_error, r2_score

- sklearn.model_selection |- train_test_split, GridSearchCV, cross_val_score
- sklearn.feature_selection |- RFE
- sklearn.linear_model |- LinearRegression, LogisticRegression, LassoCV
- sklearn.pipeline |- Pipeline

- sklearn.preprocessing |- StandardScaler
- sklearn.svm |- SVC

- sklearn.ensemble |- RandomForestClassifier, RandomForestRegressor, GradientBoostingRegressor
- sklearn.tree |- DecisionTreeClassifier
- sklearn.cluster |- KMeans

- pickle
- joblib

- matplotlib.pyplot
- seaborn


# File Descriptions

We are given the data in three files. Below is the schema and explanation of each variable in the files:

### portfolio.json - containing offer ids and meta data about each offer

- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

### profile.json - demographic data for each customer

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

### transcript.json -  records for transactions, offers received, offers viewed, and offers completed

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record


# Conclusion
   
The Capstone Project Report that will have project definition, data exploration, anlyasis, metrics, results, and conclusion. The report will be posted on Medium as a blog(link).


# Licensing, Authors, Acknowledgements


- stackoverflow website for error resolution and coding ideas
- towardsdatascience website for python concepts and coding ideas

