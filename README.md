
# Module 4 Final Project
## Modeling Tweet Sentiment

As of April 30, 2020, Twitter reported 166 million daily users. In the United States, this includes 22% of adults, who are in general young and relatively affluent. This makes Twitter an excellent resource for gauging consumer sentiment. That is the aim of this project. Using tweets about Apple and Google products were analyzed to be able to predict positive and negative sentiment. The data were analyzed by multiple Long Short Term Memory networks with different parameters. While none of the models performed ideally, the best model used a tokenizer created embedding layer, one LSTM layer with a tanh activation function and l1 regularization.  

## Business Problem

The insights provided by this model can be used to help companies determine the general sentiment surrounding their products.

## Data

This project data from CrowdFlower. The data consists of tweets about Apple and Google products rated by people as positive, negative, neutral, or unknown. The data is found in this repository and at https://data.world/crowdflower/brands-and-product-emotions. 

## Methods

The data were analyzed using multinomial Bayes, logistic regession, random forest, and recurrent neural network models. Multiple simple and LSTM models with different parameters were used to develop a network better than chance at classifying tweets. In addition exploratory data analysis provided insights about the data.    

## Results

<img src="https://raw.githubusercontent.com/charsarb/mod-4-project/master/images/wordcloudpos.jpg">
The wordcloud for the positive tweets indicated that as expected positive words like 'awesome' were fairly prominent. In addition, words related to novelty and purchase appear common.

<img src="https://raw.githubusercontent.com/charsarb/mod-4-project/master/images/wordcloudneg.jpg">
There are also a lot of words related to purchase and novelty. The modal verbs also appear more common in the negative tweets.

<img src="https://raw.githubusercontent.com/charsarb/mod-4-project/master/images/top25.jpg">
While great is in the top 25 positive words, headaches is more prominent in the negative words. Many of the positive words seems to indicate being exposed to new content (i.e. 'popup'). While some of those words appear in the negative tweets, they appear less frequently. The iphone is mentioned more in negative tweets. Interestingly, need only appears as a top word for negative tweets. Overall the words are fairly similar.

<img src="https://raw.githubusercontent.com/charsarb/mod-4-project/master/images/logregconfusionmatrix.jpg">
This model did better than chance at classifying tweets as positive or negative. It was 82% accurate.

<img src="https://raw.githubusercontent.com/charsarb/mod-4-project/master/images/nnconfusionmatrix.jpg">
This model had approximately 75% accuracy, though not stably. It was also better than chance at determining whether tweets were positive or negative. 

## Recomendations
A more complex model is not always better so using a logistic regression model is a good strategy for classifying tweets by emotion. This model is also more consistent, requires fewer resources, and performs more quickly. Having some kind of event around new products is related to positive tweets, so this is something companies should take into account if they want to see positive tweets about their product. Looking for words that are talking about taking an action may help to identify a negative tweet. Lastly, one of the best indications of a postive tweet is in fact positive words. While this seems obvious, it shows that people are often explicit about their opinions.



## Limitations

A good portion of this data came from tweets relating to SXSW, a singular event that may not paint a full picture of positive and negative tweets. In addition, because of the class imbalance, these models were trained on fairly small datasets so more data would be useful. Lastly, in this case we did not use the neutral tweet data and it should be examined in the future.