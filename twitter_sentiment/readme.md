# Twitter Sentiment Analysis

This project performs sentiment analysis on Twitter data using machine learning techniques. It utilizes a dataset containing tweets labeled as either positive or negative sentiment.

## Functionality

The project performs the following tasks:

1. **Data Cleaning**: The dataset is cleaned by removing unnecessary characters, converting text to lowercase, and removing stopwords using the NLTK library.

2. **Exploratory Data Analysis (EDA)**: EDA is performed to understand the distribution of positive and negative tweets, top users posting positive and negative tweets, and other insights.

3. **Feature Engineering**: The tweet content is vectorized using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization, which converts text data into numerical vectors.

4. **Model Training**: A Logistic Regression model is trained on the vectorized tweet data to predict the sentiment of new tweets.

5. **Model Evaluation**: The model's accuracy is evaluated using accuracy score and confusion matrix.

6. **Model Deployment**: The trained model is saved using the pickle library for future use.

7. **Tweet Sentiment Prediction**: A function is provided to predict the sentiment of new tweets. The function cleans the tweet, vectorizes it, and uses the trained model for prediction.

## Usage

1. Clone the repository: `git clone https://github.com/sv-medany/twitter-sentiment-analysis.git`
2. Ensure you have Python and the required libraries installed.
3. Run the provided Python script to perform sentiment analysis and train the model.
4. Use the `predict_tweet_reaction` function to predict the sentiment of new tweets.

## Example

```python
from twitter_sentiment_analysis import predict_tweet_reaction

# Predict sentiment for new tweets
new_tweets = [
    "Just finished a great workout at the gym! Feeling energized.",
    "Lost my wallet today. What a disaster!",
    "Enjoyed a delicious homemade dinner with my family.",
    "Feeling nervous about my upcoming job interview.",
    "Watched a hilarious comedy show tonight. Laughed so hard!",
    "Feeling grateful for the little things in life.",
    "Missed my morning train. Now I'm running late for work.",
    "Had a deep conversation with a friend. Feeling understood.",
    "Excited to start reading a new book I just bought.",
    "Feeling overwhelmed with deadlines. Need to stay focused."
]

for tweet in new_tweets:
    print(tweet)
    sentiment = predict_tweet_reaction(tweet)
    print()

