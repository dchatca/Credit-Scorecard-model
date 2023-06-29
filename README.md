# A comparison of Logistic Regression vs Adaboosting in Credit Scorecard model

In financial institutions or governments, a credit scorecard model is used to quantify an individual's or institution's profile into a credit score. Numerous methods have been employed to construct credit scorecards, with logistic regression models being the most prevalent. These models are desirable due to their robustness and transparency, but they have been surpassed in predictive accuracy by more recent techniques, such as adaBoosting. So in this project, I want to find which models is better for esstimating each customer's credit score. My study shows that there are not a big difference between these two models; the AUC of the two models are quite similar (~ 0.88), showing that two of these models' predictive ability  is good and can be applied in practice. Besides that, the accuracy of two models is also quite approximate ( ~ 0.87). 

So it’s suitable to use Logistic Regression to build a scorecard model. There are many different algorithms applied to build credit scorecard models, such as: Boosting, Neural Networks, Random Forests, and SVM. These algorithms may have better classification results, but their ability to explain the results is not good, so they are not often used to build credit scorecard models in practice. 

## Dataset

This is the modified dataset downloaded on Kaggle, I randomely choice 19881 obs in the original dataset but still keep 12 features. The target variable of this data is 'loan status', which is a binary variable (0 is non default 1 is default) 

You can find the original dataset at: https://www.kaggle.com/datasets/laotse/credit-risk-dataset

## EDA - Feature Engineering - Modeling 

The detail process can be found in my notebook.

You can access full here: https://github.com/dchatca/scorecard-model/tree/main/credit-scorecard-model

## Experimental result

Model  | TP    | TN    | F1 score | Accuracy  
-----  | ----- | ----- | -----    |-----    
LR     | 501   | 2970  | 0.66     | 0.87  
AB     | 517   | 2960  | 0.67     | 0.88  

## Futher development

We can use various Machine Learning models to compare the experiment result with the Logistic Regression such as XGboost, Catboost, LightGBM,... and even Deep Learning to get a different conclusion and find a new way to apply in the ScoreCard model. Besides that we can add a hyperparameter tuning step to get a better and better result.


