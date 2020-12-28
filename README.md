
### Abstract:
Twitter is a popular micro-blogging service, platform for public real-time communication and a perfect platform to analyze social networks. This project's aim was to use foresight trend with twitter with two keywords in mind: ai+architecture. 

Twitter has huge amount data from tweets in endless time-series. Foresight is a powerful structured foretelling that could give the possible development investment or intel to relevant stakeholders.

The projects study for insights conducted WordClouds, social network analysis and sentiment analysis. The results show rather obvious extended opportunities and forecast for the future. However, the tweets validate the intuition of future and can be used to increase the number of involved stakeholder views and to intrigue clients. While the reliability of Twitter data still requires critical reflection, this project implies that trend forecasting is probably possible with social media!


## Intro:
Twitter is both a micro-blogging service and platform for public communication. As both a social network and an information-sharing platform, Twitter offers real-time news and covers a broad spectrum of topics, for instance Elon musk tweets regularly and he a trustworthy source for information.

The limitations of the study:
- Credibility, i.e. people with a lot of followers tweets won’t be worth more than other tweets. This means that all tweets are equally and selected randomly. (However, this is an application that surely should be implemented!)
- 1000 English tweets
- Discard Retweets, since credibility what it means to retweet is rather detracted...
- Free developer version of the Tweepy-api
- Twitter was the only data source for retrieving raw data.

## Why Twitter foresight?
Because! Foresight is a structured dialogue about possible future development among relevant stakeholders. Yummy! Actually, tweets are only 140 characters of text. However, they can contain invaluable information as the data set grows. This information is not just for information-sharing, but also for searching information and examining societal change and concerns. What research is in current development, what are the previous activities regarding a topic, facilitate the search process, help to check if there is a public debate or any attention at all and if there is an intense or emotional debate going on somewhere.


![alt](https://github.com/Borg93/Twitter_trend/blob/master/data.png?raw=true)
> The figure shows the common words found based on the keywords ai and architecture


## Trend detection:
A trend describes a significant and constant development with possibly high impact on the future. Trends are relevant for foresight, especially together with environmental scanning and analyzing the state of the art. However, when using Twitter for trend recognition and prediction in the context of foresight, among others the following aspects should be kept in mind, for instance abstraction level, selective bias and obvisuly the credibility to of random tweets. Furthermore, how long are trend duration? 5 years? And how do we idenify social movements of hypes and fashions, which in contrast are short term, much attnetion and easliy disappears. However, contingent trend recognition is real and possible hypes can lead to awesome idea generations!


# The processes/results:
Raw tweets are dirty and requires text clean-up --> address case issues. In order to get relevant dataframe and a proper clean-up, the package Nltk was used. Both stopwords and collection words from the tweets are removed. Now the cleaned data can be used to analyze co-occurrence if words (i.e bigrams) and attitudes (i.e sentiments) in tweets. Bigrams are paired words from the original tweets and used to visualize the social network. 

![alt](https://github.com/Borg93/Twitter_trend/blob/master/nx.jpg?raw=true)
> The figure illustates the social network of the keywords

The network is a good way to gain quantity insight of bigrams from the tweets. In this case words are used as the nodes and the co-occurrence resembles the edges in the graph structure. There are different features of the network that can be used to gain insights from the graph. For instance, the color scheme of the network highlights the centrality of nodes, which means the degree edges connected to a node. The higher degree, the darker the color of the node. 

![alt](https://github.com/Borg93/Twitter_trend/blob/master/influence.png?raw=true)
> The figure shows the PageRank and Betweenness Centrality of the previous network

This bar graph display two different features of the network; Betweenness Centrality and PageRank. The Betweenness Centrality gives insights on the measure of a node's influence to it surrounding nodes. Furthermore, it shows the percentage of shortest paths that include a given node. PageRank, also called Eigenvector Centrality, measures the node's importance to the network. Basically, PageRank is the backbone to Google's rank web pages system, which essential gives the metric credibility. In the graph we can see that word such as hybrid, automative and artifical has both high Betweenness centrality and PageRank, which seemes very reasonable!


![alt](https://github.com/Borg93/Twitter_trend/blob/master/sent.png?raw=true)
> The figure shows the sentiment classifcation of the tweets.

Sentiment analysis is a method of identifying attitudes in text data about a subject of interest. It is scored using polarity values that range from 1 to -1. Values closer to 1 indicate more positivity, while values closer to -1 indicate more negativity. Based on this histogram, we can say that the sentiments from the keywords architecture and ai seems more positive than negative!

Finally, a WordCloud with gives an easily subjective overview of the tweets:
![alt](https://github.com/Borg93/Twitter_trend/blob/master/wc.jpg?raw=true)
> A WordCloud based on the tweets


# Conclusion:
This projected aimed to examine the potential of tweets potential for foresight of trends. However, there are more data cleaning/ NLP task to be done to get a cleaner data set to analyze.

Social media data as result of social interactions showed promising observation of the human behavior and interesting topics being discussed in the community of architecture (and this was just from 2 keywords and 1000 tweets). However, there are many different actors as firms, political parties that produce heterogeneous input covering a broad spectrum of opinions. This spread of content cannot really be captured this method and should be an interesting subject to further explore in future work. Furthermore, besides legal and ethical issues as information credibility (e.g fake news) and authenticity of the tweets can't easily be checked with the current method.

In the context of foresight, the analysis is working somewhat and could give a good spectrum of insight to influential users and stakeholders in relevant domain networks. It all comes down to expertise in domain knowledge and fine feature engineering, since the insight comes at a cost of being a creative process. However, the "golden" foresight of trends requires possible, desirable, or provocative input by the commonunty and large data-set that is livestream to capture the best future developments and trends.

# Inc Future work
The script tweetpy_streamer can actually stream calls from live from the Twitter! It currently is storing tweets in Sqlite3.db for postprocessing!
