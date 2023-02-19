# Logistic Regression for Absenteeism Prediction

Case Study provided and developed during the "Data Science Course 2023: Complete Data Science Bootcamp".
The aim of the project is to predict whether an employee of a company will be excessively absent from work or not, based on data of 12 different features across 700 unique entries. The original dataset along with its features' descriptions is provided in the .csv and the .pdf files respectively. The whole course can be found here: https://www.udemy.com/course/the-data-science-course-complete-data-science-bootcamp/ 

The approach consists of two main parts: the preprocessing phase, where targeted operations take place in order to validate, clean as well as save and prepare our source data for further analysis and the model development, where after some more data manipulation, a Logistic Regression algorithm is applied in order to achieve the desired estimations, which means results organized in a way that could give meaningful future insights. 

In the preprocessing phase, we start by giving a first glimpse over our dataset, checking for missing values and identifying some quick but useful information. Then we go deeper into manipulating the columns-features of our dataset. More precisely: 1) we drop the 'ID' feature since it bears absolutely no meaning for us, 2) we inspect the 'Reasons for Absence' column in order to group the 28 different reasons into 4 separate categories (details explained in the .pdf file), action that will significantly help us avoid multicolinearity issues in our regression later on, 3) we change the type of the 'Date' column and we extract the 'Month' and the 'Day of the Week' values since they will be more useful in our regression analysis and 4) we group the 4 different levels of education (high school, graduate, postgraduate and masters/doctors) into two main categories. Finally, we create a copy of our preprocessed dataset in a .csv format and store it in the same directory as the notebooks we are working on.

It's time for the most interesting part, the Regression's development. Before we reach that step, we need to perform some final preprocessing procedures such as separating the inputs from the target column, standardizing the inputs so that we bring them to a common scale without distorting the differences in the range of their values and lastly shuffling and splitting our dataset into train and test subsets. Next comes the training of our model which results in some useful information like the coefficients and the intercept of the Logistic Regression as well as the odds ratios of each feature, stored in a summary table ready for later analysis. In the end, after backtesting and presenting the predicted probabilities of each outcome (1: the employee will be excessively absent in the future - 0: will not), we save the model and the scaler (standardization) into an appropriate format so that we can reuse them in the future.

# Results - (Future Update)

The results will be further analyzed and visualized in Tableau in a future update, also including the deployment of the project, but with a regression score of 0.742 one could suggest that experimentation and possibly better predictions are achievable through alternative approaches such as Linear Regression or even Neural Networks.
