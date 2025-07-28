# task2-codsoft
# Movie Rating Prediction
# Author: Harshit gusain
# Batch: July
# Domain: Data Science

# Aim
The aim of this project is to build a model that predicts movie ratings based on given features.

# Datasets
The following datasets were used for this project:

Movie_data: Contains movie information after preprocessing, including MovieName, Genre, and MovieIDs.
Ratings_data: Contains ratings information after preprocessing, including Ratings and Timestamp.
Users_data: Contains user information after preprocessing, including Gender, Age, Occupation, and Zip-code.

# Libraries Used
The following important libraries were used for this project:

numpy
pandas
matplotlib.pyplot
seaborn
sklearn.preprocessing.LabelEncoder
sklearn.preprocessing.MinMaxScaler
sklearn.model_selection.train_test_split
sklearn.linear_model.LogisticRegression

# Data Exploration and Preprocessing

The Movie_data, Ratings_data, and Users_data were loaded as DataFrames from separate CSV files.
The missing values in each DataFrame were dropped using dropna(inplace=True).
The shape and descriptive statistics for each DataFrame were displayed using df.shape and df.describe().
The 'Gender' column in Users_data was encoded from categorical to numerical values using LabelEncoder.
The DataFrames were concatenated horizontally using pd.concat to create a final dataset df_data.
Unnecessary columns like 'Occupation', 'Zip-code', and 'Timestamp' were dropped from the final dataset to create df2.
Any remaining missing values in the final dataset df2 were dropped using dropna().
Data visualization was performed using count plots and histograms to gain insights into the distribution of ratings, genders, and age.

# Model Training
The feature matrix input and target vector target were created using relevant columns from the final dataset df_final.
The data was split into training and testing sets using train_test_split.
The input data was scaled using MinMaxScaler to normalize the values between 0 and 1.

# Model Prediction
A logistic regression model was initialized and trained on the training data using LogisticRegression.
The model was used to predict movie ratings for the test set using model.predict(X_test).
