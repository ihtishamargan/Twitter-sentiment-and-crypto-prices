# Twitter-sentiment-and-crypto-prices
Twitter sentiment and crypto prices prediction

Cryptocurrencies are an exponentially growing financial market and highly volatile in price. Its volatile nature makes it very difficult to do predictions by using traditional methods. Twitter is one of the most used social media platforms by crypto investors and users. In this report, we have presented a method to use Twitter to predict cryptocurrency prices using tweets sentiment analysis and historical prices data. 
We scraped and labeled tweets, preprocessed them, trained an LSTM classifier for sentiment analysis, performed statistical tests and used sentiment score along with volume of tweets to successfully predict direction and magnitude of Ethereum and Near Protocol prices. 
These predictions can be very beneficial for crypto traders and investors as they can analyze the public opinion and make better profitable decisions. 

<b>Dataset:</b>

We collected tweets dataset for two of well known cryptocurrencies, Ethereum and Near Protocol. Preprocessed tweets by using a well structured pipeline to get clean and filtered data that we required for our models.We hand labeled 3000 tweets and categorized them into ‘Neutral’, ‘Positive’, ‘Negative’ and ‘Irrelevant’ by observing the writer’s opinion or context of the tweet.
For historical prices data we have used API from coinmarketcap.

<b> Sentiment Analysis and price prediction </b>

<img src="images/sentiment analysis architecture.png" title="Sentiment Analysis Architecture">


We trained an LSTM model for sentiment analysis and fed it with our cleaned hand labeled dataset.  We got 72% testing accuracy and 84% accuracy in training and used that model to predict all other more than 350k tweets. Model classified roughly 60% of Near’s tweets and 70% of Ethereum’s tweets into neutral or irrelevant. Remaining were classified into positive and negative.

<img src="images/eth tweets distribution.png" title="Sentiment Analysis Architecture">

We performed statistical tests to check correlation between prices and tweets sentiments of our cryptocurrencies. And results showed that they are highly correlated among different features such as Volume of tweets and prices, Sentiment and change in price etc.

We then trained two more LSTM models, one was fed with only prices data and the other with both prices and sentiment data. And results showed that the model with sentiment data has performed better and in visualization we have seen the predicted pattern was much more accurate.


<img src="images/price prediction.png" title="Price Prediction">
