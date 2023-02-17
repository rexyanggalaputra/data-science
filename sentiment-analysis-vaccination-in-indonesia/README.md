# Sentiment Analysis Vaccination in Indonesia
Covid-19 vaccine is something that is highly anticipated all over the world. One of them is Indonesia. However, the presence of the Covid-19 vaccine for now has many pros and cons. The government is currently very aggressive in pushing the presence of a Covid-19 vaccine as soon as possible. Due to the impact caused by Covid-19, it can greatly worsen the condition of the Indonesian economy.
With the current presence of the Covid-19 vaccine, there has been an extraordinary response from the community. Some of these responses were also conveyed through social media such as Twitter, Instagram, Facebook, etc.

## Case Understanding
This sentiment analysis aims to find out how the public reacts to vaccination in Indonesia.

Project has some case question using the data:
1. How do people react to the vaccination program?
2. What policies should be carried out by the government?


## Data Understanding
* The datasets is about vaccination in Indonesia from Twitter started on 1/11/20 using #vaksin and #vaksinasi hastags

* The dataset consist of 13491 rows and 17 columns taken from [Kaggle](kaggle.com) platform

* [Source Data](https://www.kaggle.com/rpnugroho/indonesian-vaccination-tweets)

* Data Dictionary
  - id                : Unique id of users
  - date              : Date of tweets
  - text              : The tweets
  - hashtags          : Hashtag used
  - user_name         : Username of user
  - user_location     : Location of user
  - user_description  : Description of user
  - user_created      : Date of user account creation
  - user_followers    : Followers of user
  - user_friends      : Friends of user in Twitter
  - user_favorites    : Favorite of user
  - user_verified     : Is user verified or not
  - source            : Browser used by user
  - retweets          : How many retweets
  - is_retweet        : Is retweet or not
  - reply_to_status   : Reply

## Data Preparation
* Code Used      : Jupyter Notebook
* Library(es)    : Pandas, Numpy, NLTK, Sastrawi, Scikit-Learn, Wordcloud

## K-Means Clustering
* Finding the Optimal Number of Clusters Using Elbow Method

![download](https://user-images.githubusercontent.com/85033777/142930899-3df3616a-8e61-4a78-9ade-a6078574da67.png)

The cluster value where this decrease in inertia value becomes constant can be chosen as the right cluster value for our data. Looking at the above elbow curve, we can choose any number of clusters between 2 to 4.

## Result
### Comparison Of The number Of Clusters

![perbandingan](https://user-images.githubusercontent.com/85033777/142935011-1f9dcadc-2d3f-41f6-923e-ffd00e6ecc49.png)

From the graph above, it appears that there is a very large difference between cluster 0 and cluster 1. The results show that there are 9844 or 89.5% of data in cluster 0, while the remaining 1150 or 10.5% of data are in cluster 1.

### Cluster(s) Analysis
  - Cluster 0

![cluster 0](https://user-images.githubusercontent.com/85033777/142935018-b3e2a4ce-0553-4024-8a7b-8dc89eede6c2.png)

Cluster 0 shows that there are many words that have a 'negative' connotation. This means that there are still many people who are hesitant or do not support vaccination in Indonesia
  - Cluster 1

![cluster 1](https://user-images.githubusercontent.com/85033777/142935015-063b3468-3a6e-46eb-93d9-45e44dd6b711.png)

Cluster 1 shows that there are sets of word that have a 'positive' connotation. This means that there are people who already support the vaccination program in Indonesia

## Summary

When the vaccine was first made, which was around November 2020 to January 2021, in Indonesia there were several obstacles related to the vaccination program. Public complaints submitted through one of the social media, namely Twitter, gave a lot of comments where they were hesitant or did not support this vaccination program. After analyzing it with real life, it turns out that people still think that vaccination can have side effects on the body, therefore in the 'results' section the number of 'negative' comments is much higher than 'positive' comments.

## Policy Recommendations 

To raise public awareness of the importance of vaccination, the government can consider the following policies:

1. The local government provides socialization to the public about the importance of vaccination so that the pandemic can be immediately resolved. Socialization at the regional level can be done through villages or directly by implementing health protocols.

2. The provincial government and the ministry of health can also conduct socialization through social media and provide concrete information related to vaccination programs through the website of the ministry of health or others.

3. The government can continue the program of providing free vaccinations to the general public.
