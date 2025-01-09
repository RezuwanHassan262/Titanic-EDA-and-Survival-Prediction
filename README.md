# Practice work: Titanic Exploratory Data Analysis and Survival Prediction
This project aims to investigate the factors (Age, Class, Gender, etc)that contributed to survival in the tragic sinking of the Titanic and predict the survival chances of passengers based on some provided features.

This was the dataset [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data?select=train.csv).

The Titanic's sinking remains one of history's most infamous maritime tragedies. This project explores the Titanic dataset to identify patterns and factors influencing passengers' survival chances and tries to predict a passenger's survival chance based on those factors using different machine learning models.


This repository seeks to offer a detailed examination of the key variables involved. The features present in the dataset are,

1. PassengerId
2. Survived (target variable)
3. Pclass (passenger class)
4. Name
5. Sex
6. Age
7. SibSp (number of siblings/spouses aboard)
8. Parch (number of parents/children aboard)
9. Ticket
10. Fare
11. Cabin
12. Embarked (port of embarkation)


## Analysis and Workflow

**Data Cleaning:** Addressing missing values, fixing data types, and preparing the dataset for further analysis.  

**Exploratory Data Analysis:** Using descriptive statistics and visualizations to examine variable distributions and uncover relationships.  

**Feature Engineering:** Developing new features or modifying existing ones to represent the patterns within the data better.  

**Statistical Analysis:** Pinpointing key factors that have a significant impact on survival outcomes.  

**Survival Prediction:** Applying various machine learning models to estimate a passenger's likelihood of survival based on these factors.  

## Findings and Observations from the Data

![Survival based on Sex](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/1.png)


From the figure above, we can see that,
1. The age distribution of passengers varies across different combinations of sex and survival. For both males and females, the age distribution suggests that younger passengers were more likely to survive.
2. There might be noticeable differences in the age distributions between males and females within each survival category.

![Survival based on Class and Age](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/2.png)


From the figure above, we can see that,
1. Younger passengers in Pclass 3 have a higher density among those who didn't survive.
2. Older passengers are more prevalent in Pclass 1, and a larger proportion of them survived compared to the other classes.


![Survival based on Class and Fare](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/3.png)


From the figure above, we can see that,
1. Scatterplot indicates that the survival rates vary significantly with both age and class.
2. Passengers who paid higher fares(Pclass=1) have a better survival rate. indicated by more yellow points (survived) at higher fares.
3. Age distribution is not strongly correlated with survival as fare.


![Survival based on Gender, Age and Fare](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/4.png)


From the figure above, we can see that,
1. Younger passengers, especially females, show better survival outcomes.
2. Among males, survival appears less dependent on age compared to females.
3. Most males who survived are concentrated in the lower fare range.


![Survival of passengers genderwise for each class](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/5.png)

From the figure above, we can see that,
1. Passenger class and gender heavily influenced survival. (Females in higher classes had the best chances of survival, while males in third class fared the worst.)

![Age distribution of passengers based on Sex and class](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/6.png)

From the figure above, we can see that,
1. First-class passengers are generally older, while third-class passengers tend to be younger.
2. Female passengers often show a different age distribution compared to males, especially in third class.
3. The port of embarkation appears to influence the distribution of ages, suggesting potential socioeconomic or regional patterns.


![Embarkment point of passengers based on classes](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/7.png)

From the figure above, we can see that,
1. 1st class median line is coming around fare $80 for embarked value 'C'.

![Age distribution of passengers based on Sex and class](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/8.png)

From the figure above, we can see that,
1. Some decks (B/C) have a higher number of survivors.
2. Equal number of survivors from deck G.

![Age distribution and assigned deck of the passengers based class](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/9.png)

From the figure above, we can see that,
1. Deck A has higher proportion of older passengers in Pclass 1 compared to Pclass 3
2. 

![Family Size vs. Survival (Train split)](https://raw.githubusercontent.com/RezuwanHassan262/Titanic-EDA-and-Survival-Prediction/main/figures/10.png)

From the figure above, we can see that,
1. The singletons survived and died the most.
2. The greater the family size the less likely they are to survive.

## Predicting Survival using ML algorithms

I tried to predict the survival chances of passengers using different ML algorithms, Those are mentioned below with accuracy and relevant metrics.

|       Algorithm       |   Performance   |          Metric        |
| --------------------- |:---------------:|:----------------------:|
|  Linear Regression    |       52.6%     |          Accuracy      | 
|  Logistic Regression  |       75.6%     |       F1 score (Mean)  | 
|     Random Forest     |       10.5%     |       F1 score (Mean)  | 
| Random Forest (Hyperparameter Tuned)    |       20.3%     |       Mean Absolute Error  | 
|        AdaBoost       |       74.9%     |        F1 score (Mean)  | 
|   Gradient Boosting   |       88.9%     |        F1 score (Mean)  | 
| Custom Ensemble Model |       18.1%     |    Mean Absolute Error  |
