# Project 3 - Web APIs and NLP: Analysis on Subreddit Post of Auto Chess and Teamfight Tactics

### Overview

`Primary Learning Objectives:`
  - Using Pushshift's API to collect posts from two subreddits: AutoChess and Teamfight Tactics
  - Use NLP to train a classifier on which subreddit a given post came from. (Binary Classification)

### Problem Statement

To use NLP to train on classifier to identify which post belongs to which subreddit, Auto Chess or Teamfight Tactics.

### Background

Both Auto Chess and Teamfight Tactics and auto battler games whereby eight players will battle online with chess peices. Players will have to buy units with in-game gold, place them on a hexagonal/squared board and watch them autonomously battle against enermy players. Players will buy units from a shared unit pool and as the game goes on, players are able to place more units by leveling up, get better units and upgrade existing units. Players will lose health when losing around and deal damage if winning the round. The last player standing wins.


### General Flow of Notebook

1. Obtain data from subreddit using Pushshift's API
2. Exploratory Data Analysis 
    - 2.1 Data Cleaning
    - 2.2 Detailed text preprocessing
    - 2.3 Lemmatization
    - 2.4 Create Word Cloud
3. Modelling Random Forest
    - 3.1 CountVectorizer vs TF-IDF Vectorizer
    - 3.2 Random Forest hyperparameter tuning
    - 3.3 Naive Bayes
    - 3.4 Logistic Regression
4. Evaluation
5. Conclusion and Recommendation

### Modelling

3 different model will be analysed; Random Forest, Naive Bayes and Logistic Regression using Tfidf-Vectorizer. Hyperparameter tuning through RandomizedSearchCV and GridSearchCV by pipelining.


### Conclusion and Recommendation

In conclusion, as the dataset does not has data imbalance issue, accuracy would be a good metric in evaluating the best model for classification problem in this case. In the event of imbalanced data, the AUC score would be a better metric. Therefore, by accuracy, both random forest and Naive Bayes models perform well for this classification problem.

Recommendations:
1. For text preprocessing, we could also look into the misspelled words and also how to deal with non-english languages (chinese, vietnamese, etc,)
2. We could also possibly compare with other models such as Support Vector Machine (SVM), Neural Network, Bayesian Network etc.
3. Conduct sentiment analysis to determine whether the post is positive, negative or neutral.
4. Consider scraping Teamfight Tactics posts with different date as TFT constantly updates their patch. They have updated to Set 7 and each set has a different theme and different units with new class and origin.
