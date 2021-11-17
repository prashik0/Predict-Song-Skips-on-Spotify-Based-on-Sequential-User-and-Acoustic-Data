# Predict-Song-Skips-on-Spotify-Based-on-Sequential-User-and-Acoustic-Data

Overview

Machine learning has long been leveraged to build recommender systems to recommend music. But there has not been much research done on how a user interacts with music sequentially, throughout one listening session.
In this project, I had build a machine learning model that predicts if a user will skip a song or not given information about the user’s previous actions during a listening session along with acoustic features of the previous songs.

Dataset & Features

The first key task is to find where the data is and how to extract data so for that I had used the Spotify Sequential Skip Prediction dataset for the project, which consists of roughly 130 million listening sessions. Each session has at most 20 music tracks. 
In the dataset, all the user behavior features and track ids are provided for the first half of the session, but only the track ids are provided for the second half.
The user behavior features consist of actions like whether the user paused, hour of day, track was skipped or not, etc. and acoustic features consist of data like track metadata, danceability, tempo, beat strength, bounciness, acousticness, etc.

Data Preprocessing

I had encountered that the data is unstructured.
So to clean it and make it more meaningful I had followed below-mentioned processes.

Data Cleaning
Data Integration
Data Transformation
Dimension Reduction

EDA

In this step I had performed Exploratory Data Analysis (EDA) in which I analyzed and investigated the data and summarized their main characteristics.
For that I had followed below-mentioned processes.

Descriptive Analysis
Distinguish Attributes
Univariate / Bivariate Analysis
Correlation Between Each Attribute
Detect Outliers
Data Visualization
Feature Engineering

Feature Selection 

After EDA I had performed PCA and reduced the number of features to 30 with high percentage variance retained.

Model Building & Training

Since we were dealing with sequential data I had used following algorithms for model building and training.

1. Gradient Boosted Trees,                                                                                             
2. LSTM, Bi-LSTM 
3. Logistic Regression
 
Model Testing, Validation & Results

I had tried different models and selected the best on basis of accuracy. Also apply cross validation procedure for evaluating the wellness of model performance against the real data and develop an appropriate model accordingly.

1. Gradient Boosted Trees                                                                                        
   Accuracy on train set = 0.92, Accuracy on test set = 0.90

2. LSTM, Bi-LSTM                                                                                              
   Accuracy on test set = 0.90

3. Logistic Regression                                                                                                           
   Accuracy on train set = 0.91, Accuracy on test set = 0.90

Deployment

This was the final task, here I integrated machine learning model and integrate it into existing production environment where it can take in an input and return an output. For this I used Heroku and Flask. 
Here is the link of the app.
https://spotify-song-skip-prediction.herokuapp.com/
