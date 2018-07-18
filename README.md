# Predicting Mastery in Academic Assessments


## SUMMARY
Students taking advantage of practice exercises through various software applications seek an evaluation of their preparedness for formal academic assessments.

The goal of this project is to help test developers understand user progress by predicting whether a student answers a test question correctly. The project examines data from students preparing for three tests: the GMAT, SAT and ACT. Question fields in the dataset indicate outcome, group (test for which the student is preparing), track (test subject), sub-track, tags, question format, and times for when the question was started and answered or deactivated (timed-out). Relationships that could predict observations under the field labeled ‘correct’ are explored and modeled.

## APPROACH
1. [**Initial Data Exploration**](http://nbviewer.jupyter.org/github/humburgc/academic_mastery_study/blob/master/notebooks/initial_data_exploration.ipynb?flush_cache=true) (Data Wrangling): Download the `grockit_all_data.zip` file from the [What Do You Know? competition on Kaggle](https://www.kaggle.com/c/WhatDoYouKnow/data). Import and inspect raw training data. Isolate relevant variables, fill or calculate new variables, and organize the dataframe. Resolve missing, invalid, corrupted or duplicate values.

2. [**Exploratory Data Analysis**](http://nbviewer.jupyter.org/github/humburgc/academic_mastery_study/blob/master/notebooks/exploratory_data_analysis.ipynb?flush_cache=true): Create data visualizations to explain variables and analyze outliers. Possibly remove or mark outliers. Explore variable dependence and correlations. 

3. **Machine Learning Analysis**: Build, fit, and validate a method to model the data. Evaluate the performance of each model tested. Methods to try: Logistic Regression, Random Forest, Linear Mixed Effects, Mixed Effects Random Forest, XGBoost.


## FINAL RESULTS
EDA determined that a small number of users practiced in more than one test group; however, no overlap in questions indicates the test groups are independent. For each test group, outcomes are better across all subjects for dedicated users (attempting at least 30 questions). This effect is most dramatic for the GMAT group. Of all scenarios, average scores are best amongst the dedicated GMAT users.

Stay tuned for conclusions...

## REPORTS
* [Project Proposal](/reports/project_proposal.pdf)
* [Initial Data Exploration](/reports/initial_data_exploration.pdf)
* [Exploratory Data Analysis](/reports/exploratory_data_analysis.pdf)
* [Notebooks](/notebooks)
* [Final Report](/reports/final_report.pdf)
