# Predicting illegal drug usage from personality traits and demographic info
 
## Contents
* [Data source](https://archive.ics.uci.edu/ml/datasets/Drug+consumption+%28quantified%29)
* [Data files](Data)
* [Reference](References/The%20Five%20Factor%20Model%20of%20personality%20and%20evaluation%20of%20drug%20consumption%20risk.pdf)
* [Code/report](Drugs.ipynb)
* [Presentation](https://docs.google.com/presentation/d/1--JX88b1WO0hTc4KWwH6YXi9OkvIZe01IEJnCd_ium0/edit?usp=sharing)
* [YouTube](https://www.youtube.com/watch?v=E37Gf_O0ixI)

## Abstract
Understanding the personality traits that are predictive of illegal drug usage is important for public health and guidence of policy-making. In [Fehrman et al.](https://arxiv.org/abs/1506.06297), the authors collect survey data on demographic factors, personality traits, and drug usage, and then run several machine learning models to analyze the traits that are predictive of the usage of individual and clusters of drugs. In this project, I focused on individuals who have used drugs that are widely classified as illegal (mushrooms, ecstasy, cocaine, LSD, ketamine, heroin, and crack) at least once. Very few people will take any one of these drugs in their lifetime, so the type of person who would cross that threshold would be interesting to understand.

I trained logistic regression, decision tree, and random forest models. For each model, grid search with 10-fold cross validation was performed to find the optimal parameters with regard to balanced accuracy as the dataset was unbalanced (64% of individuals had used at least one illegal drug). The logistic regression model demonstrated that the personality traits of high sensation seeking, high openness to experience, low conscientiousness, and the demographic of men were the most predictive of illegal drug use. For the decision tree model, the first branch represented a bifuracation of individuals with higher or lower sensation seeking. For the random forest model, sensation seeking exhibited the highest permutation importance. Across models, it appears that sensation seeking is the most import feature for predicting illegal drug usage. Finally, for model evaluation, models scored between 72-78% in balanced accuracy on the test data, beating the 64% baseline; this was similar to the models described in the paper. The random forest model performed best, then logistic regression, and then decision tree.

## Project Info
<pre>
Contributors : <a href=https://github.com/aarondzt>Aaron Tan</a>
</pre>

<pre>
Languages    : Python
Tools/IDE    : Anaconda
Libraries    : numpy, pandas, matplotlib, seaborn, sklearn, statsmodels
</pre>

<pre>
Date published     : 10.12.2020
</pre>
