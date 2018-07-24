# How to create a highly-engaged reddit post?

This report provides an analysis, evaluation and suggestion for the question - How to create a highly-engaged reddit post.  
  
This is a binary classification and inferences problem based on two points:  
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

*****************************

### Description

In week four we've learned about a few different classifiers. In week five we'll learn about webscraping, APIs, Natural Language Processing, and some additional classification methods. Now we're going to put those skills to the test.

### Scenario

You're fresh out of your Data Science bootcamp and looking to break through in the world of freelance data journalism. Nate Silver and co. at FiveThirtyEight have agreed to hear your pitch for a story in two weeks!

Your piece is going to be on how to create a Reddit post that will get the most engagement from Reddit users. Because this is FiveThirtyEight, you're going to have to get data and analyze it in order to make a compelling narrative.



#### Project Summary

In this project, we will practice two major skills. Collecting data by via an API and then building a binary predictor on text data.

As we discussed earlier in the course, there are two components to starting a data science problem: the problem statement, and acquiring the data.

For this article, your problem statement will be: _What characteristics of a post on Reddit are most predictive of the overall interaction on a thread (as measured by number of comments)?_

Your method for acquiring the data will be scraping the 'hot' threads as listed on the [Reddit homepage](https://www.reddit.com/). You'll acquire _AT LEAST FOUR_ pieces of information about each thread:
1. The title of the thread
2. The subreddit that the thread corresponds to
3. The length of time it has been up on Reddit
4. The number of comments on the thread

Once you've got the data, you will build a classification model that, using Natural Language Processing and any other relevant features, predicting whether or not a given Reddit post will have above or below the _median_ number of comments.

**BONUS PROBLEMS**
1. If creating a logistic regression, GridSearch Ridge and Lasso for this model and interpret the best hyperparameter values.
2. Write the actual article that you're pitching and turn it into a blog post that you host on your personal blog.
3. Collect text comments as well to search for text "buzzwords."

---

### Requirements

- Scrape and prepare your data using the `requests` library.
- **Create and compare two models**. One of these must be a random forest, however the other can be a classifier of your choosing: logistic regression, KNN, SVM, etc.
- A Jupyter Notebook with your analysis for a peer audience of data scientists.
- An executive summary of the results you found.
- A 10-12 minute presentation outlining your process and findings for a semi-technical audience. The reason we say 'semi-technical' is that FiveThirtyEight wants to see how you plan to explain your findings in your article, and their audience is likely readers who are familiar with and interested in data / statistics, but are not experts. This means that if you'd like to talk about your model works you can, but explain what exactly your model does at a high-level.

 **Pro Tip:** You can find a good example executive summary [here](https://www.proposify.biz/blog/executive-summary).

 **Pro Tip 2:** When hitting Reddit's API, use the `sleep` function to make time in between your individual requests. **THIS IS CRUCIAL**

**Pro tip 3:** Save your results to a .csv or .txt file whenever you scrape. If you just keep your results in memory, if you computer crashes or shuts off, or you accidentally close your Jupyter notebook, you'll lose your data.

---

### Necessary Deliverables / Submission

- Code and executive summary must be in a clearly commented Jupyter Notebook.
- You must submit your slide deck.
- You must, at minimum, have a link to your slides and a link to your Jupyter notebook on your personal static site.
- Materials must be submitted by 10:00 a.m. Friday, June 1st EST.

We would like to be able to pull everyone's projects into the [master repository](https://git.generalassemb.ly/DSI-US-4/project-3) so everyone can view what anyone else in our cohort did.  In order to do this, you will need to put all of your project specific materials in their own folder within your repository (Everything thats not the `.gitignore` and `Readme.md`).  The labeling convention for this folder should be `first-last-MARKET`. 

---

#### Presentation
As the scenario states this project scenario was constructed with the intent of delivering to Nate Silver and other members of Five-Thirty-Eight (Analysts/Writers). They will have a technical understanding but also no patience for doing things incorrectly. Please, no code in the slides.  If it's something that's just so good you can't contain yourself, put it in an appendix.  Additionally, they are also writers and understand the importance of not just explaining what the data says but creating a story to wrap around the insights and bring everything together in a enjoyable and linear format. 

A good start for finding your story line is to comment your outputs very well.  The act of finding insights and noting them down (preferably in organized mark down) will help you identify a storyline and put pieces together as well as help you think about the next steps; "Based on what I just found, it would be really cool if the data turned out to lead to _____ as an insight.  I should investigate". Essentially, **narrate your project process**.  This helps you in three ways.  
- It better prepares your notebook to be a portfolio piece; the quicker a project becomes a portfolio piece, the sooner you'll be able to show it to potential employers.
- Helps you identify actions and steps you can take to approach your data to find more insights.  
- Passively helps you create a storyline that you can use when presenting. 


---

### Dataset

1. We'll be utilizing a dataset derived from live web data: [Reddit.com](https://www.reddit.com/)

2. To get the data, we will use the `requests` library.

---

### Suggested Ways to Get Started

- Read the docs for whatever technologies you use. Most of the time, there is a tutorial that you can follow, but not always, and learning to read documentation is crucial to your success!
- Document **everything**.
- Look up sample executive summaries online.

### Additional Resources
- [Advice on How to Write for a Non-Technical Audience](http://programmers.stackexchange.com/questions/11523/explaining-technical-things-to-non-technical-people)

---

### Project Feedback + Evaluation

Data science is a field in which we apply data to solve real-world problems. Therefore, projects and presentations are means by which we can assess your ability to solve real-world problems in a data-driven manner.

Your final assessment ("grade," if you will) will be calculated based on a [topical rubric](https://docs.google.com/spreadsheets/d/1V6OzSHPXCJEe_sVT7B1vE7sT-jqNMNo-NrmZHtafMXY/edit?usp=sharing). For each category, you will receive a score of 0-3. From the rubric you can see descriptions of each score and what is needed to attain those scores. Make sure you look at the "Rubric P3" tab of the [spreadsheet](https://docs.google.com/spreadsheets/d/1V6OzSHPXCJEe_sVT7B1vE7sT-jqNMNo-NrmZHtafMXY/edit?usp=sharing).

---

### Why we choose this project for you?
This project covers three of the biggest concepts we cover in the class: Classification Modelling, Natural Language Processing and Data Wrangling/Aquisition.

Part 1 of the project focuses on **Data wrangling/gathering/aquisition**. This is a very important skill as not all the data you will need will be in clean CSVs or a single table in SQL.  There is a good chance that wherever you land you will have to gather some data from some unstructured/semi-structured sources; when possible, requesting information from an API, but often scraping it because they don't have an API (or it's terribly documented).

Part 2 of the project focuses on **Natural Language Processing** and converting standard text data (like Titles and Comments) into a format that allows us to analyze it and use it in modelling. 

Part 3 of the project focuses on **Classification Modelling**.  Given that project 2 was a regression focused problem, we needed to give you a classification focused problem to practice the various models, means of assessment and preprocessing associated with classification.   




