# Airbnb-SuperHost-Prediction
Help Airbnb better define who are qualified to be a superhost and help the host better align themselves to become superhost on Airbnb by analyzing their features.

# Text Processing
1. Tolkenizing: breaks down the text into smaller chuck called tokens, which can be words, phrases or individual characters. 

2. Lemmatizing: reduce the words to its base form, which will always be a valud word, for example: running would be run.

# NLP
Analyze the text through CountVectorizer and TfidfVectorizer. CountVectorizer counts the number of times each word appears in the text and create a matrix with the result. TfidfVectorizer assigns weights to each word in the text based on how often it comes up in the text body.

# Numerical Classification based on Hotel Operation Performance
Among random forests, CatBoost, and other models, CatBoost model performed the best, achieving an f1 score of 0.81 and a precision score of 0.82 on the test set.

# Ensemble Method - Stacking
To improve our prediction accuracy for the actual superhost rate, combine the predictions generated from both textual data and numerical variables. Specifically, apply the logistic regression model to stack the best model of NLP and the CatBoost model to predict the superhost rate, with the actual superhost rate serving as the dependent feature.

The stacked model achieved an outstanding performance, with an F1 score of 0.97 and a precision score of 0.98, indicating high accuracy in detecting superhosts. The NLP prediction had the most significant impact, with a coefficient of 14.86, while the CatBoost prediction had a coefficient of 5.68. These results suggest that NLP prediction is a critical factor in accurately identifying superhosts.
