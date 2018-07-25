# GeneralAssemblyProjects

Here are 3 projects I finished in GA:

## 1. Movie Recommender System

This project is about building **a movie recommender system using neural network (Tensorflow)**. As everyone knows, recommender system is the theme of this age, we can find it everywhere from google search to Amazon, from Netflix to Spotify, to any social apps. How to build a good recommender system and improve the user satisfaction is a hot and super profitable topic in today's business world.  
  
The traditional way for building a movie recommender system is using collaborative filtering -- predict ratings based on ratings from similar users or of similar movies (cosine similarity). However, with the development of machine learning, model-based recommender system became the main trend, which not only largely improved the prediction ability by including other useful information (features), also have the ability to be continually trained when new data came in.  
  
To build a recommender system, first I built and trained a neural network -- input movie and user features to predict user ratings; and then use the movie and user feature vectors (from the NN model) to predict specific user's movie ratings and give recommendations.   
  
My model did a great job in predicting ratings. Compared with the RMSE from the collaborative filterings (User-based Collaborative Filtering: 699.96, Item-based Collaborative Filtering: 114.97), the neural network I built has a 0.94 score, which is a big improvement in terms of the prediction accuracy.
  
Based on this good model, I built a movie recommender system that have **two basic functions**:
1. For new user, recommend similar new movies by searching movie titles
2. For existing user, predict their ratings for the unseen movies and give recommendations
  
For the next step, I'm going to use a bigger database to train and improve my model, and at the same time build an interface for users to get recommendation results.

## 2. How to create a highly-engaged reddit post?

In this project, I provides an analysis, evaluation and suggestion for the question - How to create a highly-engaged reddit post. 

This question is a binary classification and inferences problem based on two points:  
1. **Target classification:** The goal is to increase the reddit post engagement rate, which can be measured by the number of comments in the post. By comparing the comment number for each post with the median number of comments, I can build a binary classification model to learn and predict the high engagement post.  
2. **Features inferences:** To answer the “How to” question, the features I’m looking for in this problem will be the drivers of engagement and can be measured by the feature importance of this classification model.
  
To solve the problem, my workflow includes three parts:  
1. **Models:** Build classification models that are possible to interpret the importance of features (e.g. KNN can’t be used) and choose one with a highest test score of accuracy.
2. **Inferences:** Analyze the result of features (coefficient / feature importance) and find the most important features that can be used to drive more engagement for reddit post.
3. **Suggestions:** Give specific suggestions to answer the how to question.  
  
Here are some findings I got from the classification modeling and the natural language processing:  
1. The top influencers of the post engagement are: 
    - Upvotes
    - Duration of posting
    - Subreddit subscribers
    - Post type
    - Stickied
    - Subreddit name
2. Text post get a higher performance on the engagement matrix: 
    - It takes shorter time to become a highly engaged post
    - It gets more comments per post on average
    - It gets more comments per hour than other types of post
    - It has a bigger chance to become a highly engaged post
    - It gets more comments per upvote on average
3. Keywords in comments shows the general topic in this subreddit  
  
Based on the findings, I made some suggestions on how to create a highly-engaged reddit post.
1. Post position: Post in the subreddits that have higher number of subscribers
2. Post type: Use text post (aka self post) is a better choice
3. Post content: Focus on the specific keywords in the comments of subreddit
  
Moving forward, I’m going to focus on these studies below: 
1. Explore the driver of text post (self post) engagement: 
    - Test post content: is there any specific words / phrases in the content driving engagement?
    - Test post title: does the title matter for text post? will it be more important than other types of post?
2. Tune and improve my model to increase the accuracy score
3. Collect more data and consider about finding new features 
4. Thoroughly Interpret model result and give more recommendations

## 3. Ames House Pricing Prediction (Kaggle Challenge)

In this project, I created a regression model based on the Ames Housing Dataset. This model will predict the price of a house at sale. ([KaggleChallengePage](https://www.kaggle.com/c/dsi-us-4-project-2-regression-challenge))

**Target:**
House price in Ames, IA (sale_price is a continuous variable)

**Problem Type:**
Regression & Predictions

**My Workflow:**
1. Inferences: Get knowledge of the most important price-related features of the property that people care about when buying a house in Ames, IA
2. Predictions: Predict the price of house at sale in Ames, IA based on the important features of the property

