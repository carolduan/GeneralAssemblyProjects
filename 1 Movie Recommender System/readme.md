# Movie Recommender System

This project is about building **a movie recommender system using neural network (Tensorflow)**. As everyone knows, recommender system is the theme of this age, we can find it everywhere from google search to Amazon, from Netflix to Spotify, to any social apps. How to build a good recommender system and improve the user satisfaction is a hot and super profitable topic in today's business world.  
  
The traditional way for building a movie recommender system is using collaborative filtering -- predict ratings based on ratings from similar users or of similar movies (cosine similarity). However, with the development of machine learning, model-based recommender system became the main trend, which not only largely improved the prediction ability by including other useful information (features), also have the ability to be continually trained when new data came in.  
  
To build a recommender system, first I built and trained a neural network -- input movie and user features to predict user ratings; and then use the movie and user feature vectors (from the NN model) to predict specific user's movie ratings and give recommendations.   
  
My model did a great job in predicting ratings. Compared with the RMSE from the collaborative filterings (User-based Collaborative Filtering: 699.96, Item-based Collaborative Filtering: 114.97), the neural network I built has a 0.94 score, which is a big improvement in terms of the prediction accuracy.
  
Based on this good model, I built a movie recommender system that have **two basic functions**:
1. For new user, recommend similar new movies by searching movie titles
2. For existing user, predict their ratings for the unseen movies and give recommendations
  
For the next step, I'm going to use a bigger database to train and improve my model, and at the same time build an interface for users to get recommendation results.

**Note:**
1. Code.ipynb: my notebook
2. Presentation_tech.pdf: my tech presentation deck
3. Presentation_non_tech.pdf: my non-tech presentation deck