# How to create a highly-engaged reddit post?

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

**Note:**
1. Code.ipynb: my notebook
2. Presentation.pdf: my presentation deck