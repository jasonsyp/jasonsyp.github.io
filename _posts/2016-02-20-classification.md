---
layout: post
title: European Dis-Union...Topic Modeling with Twitter
---
This is the penultimate project before....the Final Project!, signifying the end of our bootcamp journey.  It's crazy to think that the finish line is so near, it seems like just yesterday we were stumbling through the starting blocks of this marathon called Data Science.  Nevertheless, this is NYC, and the show must go on...

For this project, we applied unsupervised machine learning and natural language processing.  We were also introduced to collecting data with API's and NoSQL databases and were encouraged to employ them for this effort.  With that in mind, I decided to focus on collecting Twitter data relating to the European Union (EU). Given the current turmoil in Europe regarding the Syrian refugee crisis, the upcoming UK referendum on leaving the EU, and the fact that I have family in Europe, I wanted to examine what the "Twitter-verse" was saying regarding the EU. The basic premise was: assume you were a consultant for a U.S. client who was looking to expand operations into Europe. While the financial data looked promising, your task was to examine the geo-political situation and provide a recommendation.

Twitter can be leveraged as a real-time news source, often providing updates on current events before the traditional media. Of course, this assumes you are following accounts that tweet such information, or search relevant hashtags. Hashtags are essentially Twitter's version of topic modeling (spam notwithstanding). But I went into this project assuming I had none of this information. My goal was to leverage the Streaming API and collect all tweets pertaining to the EU, using just the keywords "European Union and EU", and then apply K-Means Clustering and Latent Dirichlet Allocation (LDA) to determine relevant topics from all the tweets collected.

I configured a Python script to run remotely on my AWS EC2 instance, using the Tweepy library to access the Streaming API (why be RESTful when you can Stream!). For over 36 hours, tweets were collected and loaded into a MongoDB NoSQL database also hosted on EC2.  For analysis, I applied K-Means Clustering and Latent Dirichlet Allocation(LDA) topic modeling to see exactly what all these tweets were saying.  I used the Python pyLDAvis library to visualize the topics.  For a general perspective of the most frequent words in the tweet corpus, here's a simple word cloud created in Python:

<figure class="full">
    <a href="/images/word_cloud.png"><img src="/images/word_cloud.png"></a>
    <figcaption><center>Word cloud of tweets on the European Union</center></figcaption>
</figure>

On a comical side note, this project also boosted my foreign language skills unintentionally.  While I set my stream to only collect tweets in English, after noticing a large concentration of tweets from Brazil, I am now aware that "eu" is the Portuguese pronoun "I".  The learning never stops...
