# Predicting-Airline-Passengers-Satisfaction-with-Classification-Algorithms
Accomplished data cleaning and preparation such as:
- Column names are renamed.
- Elements in Features 'Customer Type' and 'Class' are renamed.
- Rows with Null values ​​are removed.
- Rows with scores of 0 in the survey of satisfaction are removed (Customers probably did not indicate).
- Departure Delay and Arrival Delay are combined.
- Satisfaction target is relabeled as 0 and 1.
Accomplished Feature Selection and Exploratory Data Analysis by Creating visualizations to first understand the business problems, and also identify important features for model building:
- Find out the proportion of classes in target, and split them by Type of Travel and Type of Customers (To understand the trend of satisfaction - useful later in model evaluation)
- Identify feature significance for the model through visualizing KDE plots, LASSO paths, and heatmaps.
- After evaluation and discreet selection, I have decided to drop 'Gender, 'Total Delay','Flight Distance','Age','Gate Location' and 'Departure/Arrival Time Convenience'
Accomplished Model Selection by finding out the best model for the data through Regularization, Cross Validation with an evaluation with an f1 score:
- Logistic Regression (find out the best C)
- KNN (find out the best k)
- Gaussian Naive Bayes
- Decision Trees (find out the best depth)
- Random Forest (find out the best depth; no. of trees did not improve the model significantly)
- Ensemble (Taking all the models with the best hyperparameters)


The result is Random Forest is selected as the best model, but Simple Validation is conducted to tune the probability threshold:
- When the threshold increased from 0.5 to 0.7, better precision is obtained from 97% to 99%
- We need the best precision for our business solution
