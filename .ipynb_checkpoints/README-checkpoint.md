# ![](./code/img/intro.png)

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Subreddit Classification

## Problem Statement:
According to Wikipedia "Reddit is an American social news aggregation, web content rating, and discussion website". Reddit is divided into subreddit that covers different topics. 

In this project, we will look at post titles from two subreddits: **NBA** and **Soccer**, and build a classification model to predict if given a post title, what subbreddit it came from (NBA or Soccer).

### Table of Contents
- [Data Collection](#Data_Collection)
- [Exploratory Data Analysis](#EDA_and_Data_Cleaning)
- [Data Visualization](#Visualization)
- [Modeling](#Modeling)
- [Interpretations](#Interpretations)

## Data Dictionary

| Feature | Data Type |Description
| --- | --- | --- |
| title| object |title of the post.
| created_utc | int64 |Date/time stamp for post creation (can be converted into Date/Time)
| selftext | object |body of the post.
| author | object |author of the post.
| media_only | bool |post containing only media.
| permalink | object |link to the post.
| Target | int64 |NBA: 0, Soccer:1.

## Model selection:
In this project I tried several classification models to predict subreddit posts, these models were:
- Logistic Regression
- Naive Bayes
- Random Forest

Here's a summary of the results obtained by each model

|                     | Training score | Testing score | Precision | Accuracy |
|---------------------|----------------|---------------|-----------|----------|
| **Logistic Regression** | 0.998          | 0.968         | 0.971     | 0.968    |
| **Naive Bayes**         | 0.989          | 0.971         | 0.980     | 0.971    |
| **Random Forest**       | 0.999          | 0.960         | 0.966     | 0.960    |

## Interpretation 
- Naive Bayes was the best performing model, it increased accuracy and precision.
- Logistic regression also performed well but more tuning is needed to improve the model.
- Random forest did not perform well as it lead to overfitting the training model with reducing the accuracy and precision scores.

## Future work:
- Trying other classification models (e.g. SVC)
- More tuning with hyperparameters to improve models
- Include lemmatization and stemming
- Streamlit, to make the model available for use 

## Refrences:
- https://en.wikipedia.org/wiki/Reddit
- https://pushshift.io/
- https://www.reddit.com/r/nba/
- https://www.reddit.com/r/soccer/
