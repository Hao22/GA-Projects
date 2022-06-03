# Project 3 - Web APIs & NLP


## Executive Summary

The world is evolving rapidly in current times as the impact of technology trends become more prevalent in our daily lives. Boosted by the COVID-19 crisis, companies are investing heavily in technology and in turn sped up the adoption of digital technologies. As a result of the rapid changes, many jobs were suddenly made redundant and new jobs requiring particular digital skills were in huge demand to fill the employment gap. In the midst of this, many positions requiring skillsets such as data science, digital marketing, web development and software development were created in response to the new employment trend.

## Problem Statement

As a business analyst with General Assembly, a private organizational entity which specializes in digital upskilling and career transformation, you are tasked to follow up on the current trends in digital upskilling by scraping text data from online forums such as Reddit, and build a text classifier model to identify if a particular post belongs to the data science or digital marketing subreddit. By understanding if there are more meaningful chatter regarding either topic, it gives us an understanding of the popularity and relevance of each skillset and allows General Assembly to better allocate resources to improve the curriculum offered.

## Approach

20,000 posts per subreddit were scraped with the use of Pushshift API, a free API which allows the collection of text data from Reddit. Data cleaning and exploratory data analysis were performed to give an understanding of the data we collected with the API. A FacetGrid was plotted to have a quick overview of the distribution of text length and word counts of the posts that we collected, and noticed most submissions having shorter length and word counts. However, the decision was made to keep the outliers which represented posts with much longer lengths and higher word counts, as it should not affect model performance due to it being a more qualitative analysis rather than quantitative.

Further preprocessing methods were applied to the text information by expanding contracted words such as 'don't' to 'do not'. Special characters, numbers and stopwords were removed, lemmatizating the text data to reduce the words to their root form were also carried out.

## Modelling

We then vectorized the final text dataset with either CountVectorizer or TF-IDF Vectorizer and modelled the text matrices with Multinomial Naive Bayes (MultinominalNB), Random Forest and Support Vector Machines model. We compared the performances of each model when used with either vectorization method and the summary of the results are shown below:

|Model|Train Accuracy Score|Test Accuracy Score|
|---|---|---|
|Baseline model|50.71%|
|Multinomial Naive Bayes and CountVectorizer|94.75%|94.90%|
|Multinomial Naive Bayes and TF-IDF Vectorizer|94.63%|94.72%|
|Random Forest and CountVectorizer|91.40%|91.10%|
|Random Forest and TF-IDF Vectorizer|91.21%|90.69%|
|Support Vector Machines and CountVectorizer|96.14%|94.42%|
|Support Vector Machines and TF-IDF Vectorizer|98.55%|95.23%|

Accuracy score was chosen to be the evaluation metric for comparing model performances as we are interested to evaluate how well our model can correctly classify if a text data belonged to either r/datascience or r/digitalmarketing.

The Support Vector Machine model using TF-IDF vectorization was selected as the best model based on the highest test accuracy score of 95.23%. Although there was a slight overfitting issue with this model, it still managed to achieve the highest test accuracy score, and the difference in accuracy scores between training and testing sets was within reasonable range. 

## 9. Conclusions and Recommendations

In summary, we recommend to utilize the Support Vector Machines model to classify if a particular post belonged to either subreddit, with our model achieving a respectable accuracy of 95.23%. This meant that for every 10,000 posts run through our model, we expect the model to predict 9523 posts correctly that they belonged to a particular subreddit.

Our model allows us to classify whether a particular text belonged to either subreddit/topic, so that the lead instructor(s) would not have to manually read every single post to understand the current educational trend. However, merely building the model is insufficient to achieve our project goal, as we are still unable to understand the current trend. Some additional work could be done to achieve this, such as collecting posts and/or comments within a particular time period(eg. 3 month period), and establishing if there were more submissions belonging to either subreddit, as well as to conduct a sentiment analysis to analyze user's perspective towards a particular topic.
