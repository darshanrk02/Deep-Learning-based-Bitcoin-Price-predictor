# Deep-Learning-based-Bitcoin-Price-predictor

It is  a deep learning model that uses past Bitcoin prices and related tweet sentiments to predict Bitcoin price.

**Data set:**
1. **bitcoin_dataset.csv:** The dataset consists of Opening, Closing, High, Low prices and Volume of Bitcoin from 02-03-2022 to 02-03- 2023. The dataset is sourced from Yahoo Finance. 
2. **bitcoin-tweets-16m-tweets-with-sentiment-tagged.csv:** This dataset consists of around 16 million Twitter tweets related to Cryptocurrency from 01-01-2016 to 29-03-2019. This dataset is sourced from Kaggle.
   
Link to data set: https://www.kaggle.com/datasets/gauravduttakiit/bitcoin-tweets-16m-tweets-with-sentiment-tagged

This project consists of several steps
1. **Data pre-processing:** It involves finding and filling out NAN values in the price data. It also involves lemmatizing tweets and obtaining word embeddings from these tweets.
2. **Advanced data pre-processing:** It invloves analysing covariance, correlation of Opening, Closing, High and Low prices of Bitcoin and applying PCA to these components to get single representative component of all these data.
3. **Building base price prediction model:** It invloves developing price prediction model only using past Bitcoin data. Stacked LSTMs are used for this purpose.
4. **Building price prediction model with sentiment scores:** It involves developing price prediction model using both past Bitcoin data and sentiments of tweets. It uses pre-trained models like VADER, RoBERTa, TextBlob and Flair to get sentiment scores, which are then used with past Bitcoin prices to predict the prices.

NOTE: It was found that VADER performed well in obtaining sentiment scores due to its domain specificity in analyzing sentiments within social media texts.

Results Obtained:

![image](https://github.com/darshanrk02/Deep-Learning-based-Bitcoin-Price-predictor/assets/97380105/53ba2e2c-514a-4272-b641-860343fe2b05)

![image](https://github.com/darshanrk02/Deep-Learning-based-Bitcoin-Price-predictor/assets/97380105/d10139b5-32d6-4b12-9076-f1bc24befc61)

The blue line in Fig above represents the actual price of Bitcoin, the orange line represents the predicted price of Bitcoin for train data and the blue line represents the predicted price of Bitcoin for test data.

