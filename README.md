
# Module 4 Final Project
## Modeling Tweet Sentiment

As of April 30, 2020, Twitter reported 166 million daily users. In the United States, this includes 22% of adults, who are in general young and relatively affluent. This makes Twitter an excellent resource for gauging consumer sentiment. That is the aim of this project. Using tweets about Apple and Google products were analyzed to be able to predict positive and negative sentiment. The data were analyzed by multiple Long Short Term Memory networks with different parameters. While none of the models performed ideally, the best model used a tokenizer created embedding layer, one LSTM layer with a tanh activation function and l1 regularization.  

## Business Problem

The insights provided by this model can be used to help companies determine the general sentiment surrounding their products.

## Data

This project data from CrowdFlower. The data consists of tweets about Apple and Google products rated by people as positive, negative, neutral, or unknown. The data is found in this repository and at https://data.world/crowdflower/brands-and-product-emotions. 

## Methods

The data were analyzed recurrent neural networks. Multiple LSTM models with different parameters were used to develop a network better than chance at classifying tweets. In addition exploratory data analysis provided insights about the data.    

## Results

The random forest model with modified hyperparameters provided the best balance of metrics and was 88% accurate.  

![wordcloudpos](Images/wordcloudpos.jpg)
The wordcloud for the positive tweets indicated that as expected positive words like 'awesome' were fairly prominent. The product names also featured heavily. 

![wordcloudneg](Images/wordcloudneg.jpg)
Some of the brand names seemed larger in this wordcloud but further analysis did not bear this out. 

![top25](Images/top25.jpg)
The ipad is the most discussed product both positively and negatively. Contrary to the appearance in the wordcloud, Apple is mentioned more in positive tweets while Google is more mentioned in the negative tweets. While great is in the top 25 positive words, headaches is more prominent in the negative words. Many of the positive words seems to indicate being exposed to new content (i.e. 'popup'). While some of those words appear in the negative tweets, they appear less frequently. The iphone is mentioned more in negative tweets. Interestingly, need only appears as a top word for negative tweets. Overall the words are fairly similar.

![model](Images/model.jpg)
While the model did not perform idealy, this model had approximately 80% accuracy, though not stably. 

## Recomendations
Having some kind of event around new products is related to positive tweets, so this is something companies should take into account if they want to see positive tweets about their product. Looking for words that are talking about taking an action may help to identify a negative tweet. Lastly, one of the best indications of a postive tweet is in fact positive words. While this seems obvious, it shows that people are often explicit about their opinions.



## Limitations

A good portion of this data came from tweets relating to SXSW, a singular event that may not paint a full picture of positive and negative tweets. In addition, because of the class imbalance, these models were trained on fairly small datasets so more data would be useful. Lastly, in this case we did not use the neutral tweet data and it should be examined in the future.