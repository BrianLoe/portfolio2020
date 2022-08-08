# COMP2200/COMP6200-S2-2020 Data Science Portfolio @ Macquarie University
#### Name: Cornelius Brian Loe  
#### SID: 45710783

This repository will hold your portfolio projects for this semester. You should customise this README.md file to document your own work - add your name and details and describe what you've done. This will be displayed on your Github page.

Portfolio projects

## Porfolio 1: Analysis of CSV data for cycling  
### Summary: 
There are 3 datasets which are used in this analysis, they are strava, GoldenCheetah, and weather datasets. The datasets about rides are from strava and GoldenCheetah. The data provide analytics services over ride data starting from January 2018. Both dataset has some of the same variables. The weather datasets are used to correlate the temperature with some of the variables in rides datasets. Here we analysed the distributions, correlations, differences in types, and the relationship between the temperature provided by the weather datasets and correlate it with some of the rides' variables.
- For key variables (time, distance, average speed, average power, TSS) they have skewed distribution. From the 5 variables, 3 of them (time, distance, TSS) have a positive skewed distribution. While the remaining variables (Average speed, average power) have negative skewed distribution.

- For correlations: 
  * Distance have a strong relationship and positive correlation with `moving_time`, `TSS`, and `Elevation Gain`. 
  * Moving Time have a strong relationship and positive correlation with `TSS` and `Elevation Gain`. 
  * Average Speed have a strong relationship and positive correlation with heart rate, power, and Normalised Power.
  * Heart rate have a strong relationship and positive correlation with power and normalised power.
  * Power have a strong relationship and positive correlation with normalised power.
  * TSS have a strong relationship and positive correlation with `Elevation Gain`.
                    
- For differences in workout type categories I took distance, moving time, average speed, average power, average cadence, and normalised power as a variable that I found interesting. There are some interesting outcome of those variables. In comparing those variables, workout type correlate differently with each variable. There are some interesting differences in the workout types.

- For the relationship between weather and rides, both distance and average speed per ride seems to have a little correlation. For distance per ride, correlation score shows that it is a positive correlation but the correlation score is very close to zero. For average speed per ride, correlation score shows that it is a negative correlation but the correlation score is very close to zero.

Challenge:
- For variable that lead to more kudos there are several variables that lead to more kudos. The variables are `Distance`, `moving_time`, `Duration`, `Elevation Gain`, `TSS`, `Calories (HR)`. They have a strong relationship with kudos. However the most impactful variable is distance. Therefore distance is the variable that lead to more kudos. 
- For TSS and Km ridden it peaks around November and December 2018 which could mean that riders seems to have a high TSS when ridden for a long distance. Meanwhile in other months for Km ridden it looks stable under 500km ridden each month. For TSS it drops a lot between July and August 2018 and looks stable when reaching February-March 2019 and it continuously looks stable afterwards.

## Portfolio 2: Analysis of Energy Usage of a House Based on Internet of Things (IoT)
### Summary:
The datasets are already been splitted to train and test which are provided. The datasets are about energy usage of a house based on Internet of Things (IoT). They are from the year 2016 and the dates start from January. Here we are predicting the energy usage using linear regression. There are some exploration showing the distribution of variables after showing the linear regression model and it's evaluation metrics. We analysed the correlation between variables using pairplots and we also used Recursive Feature Estimation (RFE) to select the optimal number of features.  
- Linear Regression model on test model shows that the scores drop a little from train model. The scores match with the provided on paper. Residual plot for test model seems to have a pattern and an outlier which seems to not support the linear model.
- Distribution plot match with the provided on paper. The distribution for energy consumption seems to be skewed. On the boxplot, there seems to be many outliers.
- Pairplots are used to show correlation between variables and the distribution of each variables. They are splitted to 4 pairplots to fit all variables:
  * First Pairplot shows 8 variables to correlate. `Appliances` has some correlation with the other variables although it is low. Indoor rooms' temperature are correlated with each other.
  * Second Pairplot showed 7 variables to correlate. Here Rooms' temperature are correlated to each other. `Appliances` has a low correlation with the other variables.
  * Third Pairplot shows 7 variables to correlate. There is nothing particular to mention for `Appliances` correlations. Rooms' temperature are correlated to each other and there are some negative correlation.
  * Fourth Pairplot shows 9 variables to correlate. Here there are positive correlation and negative correlation between the variables.
- Heatmaps showed the energy consumption for the first 4 weeks which are separated to 4 heatmaps. For overall first 4 weeks, there are some pattern at night where energy use is high except for week 3 where the energy use is high only at the weekends.
- For RFECV the results here are different with the provided. Here the RFECV scores are more higher. Also the optimal number of predictors here are smaller.

## Portfolio 3: Predicting the Genre of Books from Summaries
### Summary:
The dataset is used by grouping them into 5 targeted genres. Then I use the summary to predict which genre is the book suited in. The 5 targeted genres are: Children's literature, Science Fiction, Novel, Fantasy and Mystery. I used 4 models here which are Logistic Regression, K-nearest neighbours classifier, Gaussian naive bayes and Random forest classifier. First we extract the words that appear frequently from summary so the model can predict better.
- For Logistic regression model, they give the best accuracy of all 4 models. Their confusion matrix is also pretty good with only a small proportion of false positives and negatives. Moreover, the evaluation metrics are also pretty good.
- For K-nearest neighbours, they give the worst accuracy of all 4 models. Their proportion of false positives and negatives are pretty high compared to the other models. Their metrics scores are also not balanced.
- For Gaussian naive bayes, their accuracy is near logistic regression model. This model is good enough to predict genres. As for the confusion matrix, their proportion of false positives and negatives are quite low but not as low as logistic regression model.  
- For Random forest classifier, their accuracy is more nearer to logistic regression model and considered to be second highest here. Though, their metrics score and confusion matrix are odd. Thus, this model is not considered to be one of the good models.

Overall, logistic regression model gives better accuracy in predicting genres than the other three models followed by gaussian naive bayes.
