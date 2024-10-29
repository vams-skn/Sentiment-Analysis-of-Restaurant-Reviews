# Sentiment Analysis of Restaurant Reviews
This project aims to develop a machine-learning model to detect the sentiment of a customer’s review of a restaurant. The review is in a textual form and the model should understand the review's sentiment and automate a result. The result will be either positive or negative.

The [Kaggle dataset](https://www.kaggle.com/datasets/d4rklucif3r/restaurant-reviews) used to train the models consists of 1000 reviews from a restaurant.

For example, if the review given by the user is:

>Excellent food! The menu is extensive and seasonal to a particularly high standard. Definitely fine dining. It can be expensive but worth it and they do different deals on different nights so it’s worth checking them out before you book. Highly recommended!

The model should detect that this is a positive review. Thus the output for this text will be Positive.

## Model Training Process
Before we train our NLP model, we must clean the text in the dataset. This includes:
1. Removing unnecessary punctuation marks except apostrophes.
2. Removing stopwords of english, which are commonly repeated words that hold no meaning to our model.
3. Changing the case of all text in to lower case.
4. Stemming the words in order to get the root of the word, to optimise the sparse matrix that will be formed by the CountVectoriser.
5. Making the Bag Of Words model by using the CountVectoriser class imported from sklearn.
6. Training our classification models:
	1. Logistic Regression
	2. Naive Bayes

### Naive Bayes Algorithm
Naive Bayes is the most used algorithm in natural language processing (NLP) problems. It calculates the probability of each tag for a given sample and then gives the tag with the highest probability as output.

### Random Forest Classification Algorithm
In Random Forest Classification, multiple decision trees are created using different random subsets of the data and features. Each decision tree is like an expert, providing its opinions on classifying the data. Predictions are made by calculating the prediction for each decision tree and then taking the most popular result.

## Conclusion
The Random Forest Classifier predicted sentiments with 72% accuracy.
The Naive Bayes model predicted sentiments with a best accuracy score of 78.5% with an Alpha value of 0.2.