Developing Data Products Project - Predicting Survival (Titanic Disaster)
========================================================
author: Shashank Salvi
date: 21 June 2015
transition: rotate

Brief Overview
========================================================

The sinking of the RMS Titanic is one of the most infamous shipwrecks in history.  On April 15, 1912, during her maiden voyage, the Titanic sank after colliding with an iceberg, killing 1502 out of 2224 passengers and crew.

![image of Titanic](DSDataProductPresentation-figure/300px-RMS_Titanic_3.jpg)

Objective of this application, is to analyze what sorts of people were likely to survive. The application uses machine learning algorithms to predict which passengers were likely to have survived the tragedy.

Titanic Data set
========================================================
* Data Details :

The Titanic data set used in this Application, contains passengers information alongwith the passengers survival status. Following is summary of the dataset :

```
'data.frame':	891 obs. of  12 variables:
 $ PassengerId: int  1 2 3 4 5 6 7 8 9 10 ...
 $ Survived   : int  0 1 1 1 0 0 0 0 1 1 ...
 $ Pclass     : int  3 1 3 1 3 3 1 3 3 2 ...
 $ Name       : Factor w/ 891 levels "Abbing, Mr. Anthony",..: 109 191 358 277 16 559 520 629 416 581 ...
 $ Sex        : Factor w/ 2 levels "female","male": 2 1 1 1 2 2 2 2 1 1 ...
 $ Age        : num  22 38 26 35 35 NA 54 2 27 14 ...
 $ SibSp      : int  1 1 0 1 0 0 0 3 0 1 ...
 $ Parch      : int  0 0 0 0 0 0 0 1 2 0 ...
 $ Ticket     : Factor w/ 681 levels "110152","110413",..: 525 596 662 50 473 276 86 396 345 133 ...
 $ Fare       : num  7.25 71.28 7.92 53.1 8.05 ...
 $ Cabin      : Factor w/ 148 levels "","A10","A14",..: 1 83 1 57 1 1 131 1 1 1 ...
 $ Embarked   : Factor w/ 4 levels "","C","Q","S": 4 2 4 4 4 3 4 4 4 2 ...
```

Machine Learning Algorithm
========================================================
Analysis Details :

The application will use the ***rpart*** library in R. Recursive partitioning is a fundamental tool which helps explore the stucture of a dataset, while developing easy to visualize decision rules for predicting a categorical (classification tree).


```
function (formula, data, weights, subset, na.action = na.rpart, 
    method, model = FALSE, x = FALSE, y = TRUE, parms, control, 
    cost, ...) 
NULL
```

TitanicSurvivalApp - Data product
========================================================
TitanicSurvivalApp is a Shiny Data Application which provides function to analyze and train a predictive model for survival of a passenger. It allows user to compare accuracy of different models and select a appropriate model for prediction. It has two functions as follows:

* ***Exploratory Analysis*** : This function allows to view summary and distribution of a selected variable from the dataset.
* ***Predicitive Model*** : This function trains a model for selected variables and also displays a visual representation of the classification tree.

Click [Here](https://shashanksalvi.shinyapps.io/TitanicSurvivalApp) to Start Application.
