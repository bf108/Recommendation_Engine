# Recommendation Engine for articles on IBM Watson Platform

## Introduction
The aim of this project is to build a recommendation engine to be used on real data from the IBM Watson Studio platform. Recommendations will be made based on different approaches.

- Ranked based recommendations (articles with most user interactions)
- Collaborative filtering recommendations (finding similar users and suggesting articles not seen by one)
- Content based recommendations (classifying articles of interest and recommending articles in that category which have not been seen by the user)
- Finally we will look at predictive recommendations using Singular Value Decomposition (SVD)

## Dataset
The data for this project was provided by [Udacity Data Science Nanodgree](https://www.udacity.com/course/data-scientist-nanodegree--nd025) in partnership with IBM Watson Studio

Information for the assignment consisted of 1051 unique articles and 5149 unique users.

# Approach to recommendation engine
Ranked Based
The dataset doesn't provide details on whether the users liked or disliked the articles. An assumption was made that any user article interaction is a positive one, therefore articles with a higher number of interactions are defined as more popular overall. This defines the ranked based recommendation approach.

Collaborative approach
To recommend articles to users based on similar users, we created a user_article matrix. This matrix allowed us to determine most similar users. Once we determined similar users, we could then check to see if there were any articles that they had read, which the user we were recommending for had not.

Content Based
We will apply some natural language processing to the body of the documents in an an attempt to classify them. Once classified, it will enable us to determine similarity of other documents and recommend them.

As the original dataset articles were unclassified, this lent itself to an unsupervised ML to classify the articles.

Predictive recommendations
This approach utilised Singular Value Decomposition to predict user article interactions.
