# Predicting Mastery in Academic Assessments


## SUMMARY
Students taking advantage of practice exercises through software applications seek an evaluation of their preparedness for formal academic assessments. The goal of this project is to help test developers understand user progress by predicting whether a student answers the next test question correctly. 

Data are from students preparing for three test groups - ACT, GMAT and SAT. Question fields in the dataset indicate outcome, group, track (test subject), sub-track, ‘game’ structure, and times for when the question was started and answered or deactivated. Relationships that could predict observations under the field labeled correct are explored and modeled throughout the project.

## APPROACH
1. [**Initial Data Exploration**](http://nbviewer.jupyter.org/github/humburgc/academic_mastery_study/blob/master/notebooks/initial_data_exploration.ipynb?flush_cache=true) (Data Wrangling): Download the `grockit_all_data.zip` file from the [What Do You Know? competition on Kaggle](https://www.kaggle.com/c/WhatDoYouKnow/data). Import and inspect raw training data. Isolate relevant variables, fill or calculate new variables, and organize the dataframe. Resolve missing, invalid, corrupted or duplicate values.

2. [**Exploratory Data Analysis**](http://nbviewer.jupyter.org/github/humburgc/academic_mastery_study/blob/master/notebooks/exploratory_data_analysis.ipynb?flush_cache=true): Create data visualizations to explain variables. Detect and possibly remove or mark outliers. Explore variable dependence and correlations. Consider a hypothesis to explore. Leverage statistical inference to test the hypothesis. More generally, begin to develop a preliminary likeness of the solution 

3. [**Machine Learning Analysis**](http://nbviewer.jupyter.org/github/humburgc/academic_mastery_study/blob/master/notebooks/machine_learning_analysis.ipynb?flush_cache=true): Build, fit, and validate a method to model the data. Evaluate the performance of each model tested, including Logistic Regression, Random Forest, Linear Mixed Effects, Mixed Effects Random Forest, XGBoost.


## FINAL RESULTS
EDA determined that a small number of users practiced in more than one test group, but also indicated that test groups are independent which was confirmed by hypothesis testing. For each test group, outcomes are better across all subjects for dedicated users (attempting at least 30 questions). This effect is most dramatic for the GMAT group. Of all scenarios, average scores are best amongst the dedicated GMAT users. 

XGBoost was the best model by both measures, so it was then used to fit data filtered for dedicated users. Both performance measures improved. Accuracy: **0.7109**  CBD: **0.2411**

![Strongeset Features from the Best Model: XGB for Dedicated Users](/reports/figures/strongest_features.png)

## REPORTS
* [Project Proposal](/reports/project_proposal.pdf)
* [Notebooks](/notebooks)
* [Initial Data Exploration](/reports/initial_data_exploration.pdf)
* [Exploratory Data Analysis](/reports/exploratory_data_analysis.pdf)
* [Final Report](/reports/final_report.pdf)
* [Slide Presentation](/reports/presentation.pdf)
