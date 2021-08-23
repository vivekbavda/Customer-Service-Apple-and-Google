# Bavda Consulting

# Vivek Bavda

# Apple or Google: Who Has the Customer Service Edge?

## Problem Statement

As you are aware, Mr. Amir Payeebaj of ANEC-NOC, customer service is the cornerstone of your business. Given your desire to grow your customer base with better customer service, you've asked Bavda Consulting in a multi-part project to analyze the customer service of Apple and Google to help you choose who you should use as the model for your organization. In our discussions, it is my understanding that you wish to target the readers of Reddit to determine if there is any significant difference in language that would suggest that one company's customer service responses may be better than the other. 

Recommendation: There are differences in language in these two subreddits, but both are good.. Use the Random Forests model to choose Apple or Google customer service by entering  you company's subreddit posts or a targeted subreddit posts and see whether the model predicts Google or Apple. By identifying your customers' needs and desires, this model could guide you to which company to imitate. 

## Table of Contents in the Repository

A Jupyter Notebook 
[BavdaConsultingNLPDataCollection](https://git.generalassemb.ly/vivekbavda/project_3/blob/master/BavdaConsultingNLPDataCollection.ipynb) showing the introduction, background, outside research, data set information, and data collection function & process.

A Jupyter Notebook 
[BavdaConsultingNLPDataCleaning](https://git.generalassemb.ly/vivekbavda/project_3/blob/master/BavdaConsultingNLPDataCleaning.ipynb) showing the Exploratory Data Analysis, Data Cleaning, and Summary Statistics & Visualizations Created.

A Jupyter Notebook [BavdaConsultingNLPModelingConclusions](https://git.generalassemb.ly/vivekbavda/project_3/blob/master/BavdaConsultingNLPModelingConclusions.ipynb) showing the detailed calculations and analysis

The Data Folder in this repository contains three datasets:

- apple818.csv: This dataset was generated on August 18, 2021 from a query of customer service in the Apple subreddit through an API custom function for Reddit.  This ensured that data was collected automatically. Moreover, the function has a three second timer to prevent overwhelming Reddit's server. This is a raw dataset that contains columns that were not used. However, most of these were eliminated in data cleaning and exploratory data analysis. The key portion was the text posts. This dataset was merged with google818.csv to create modeling.csv.


- google818.csv: This dataset was generated on August 18, 2021 from a query of customer service in the Google subreddit through an API custom function for Reddit.  This ensured that data was collected automatically. Moreover, the function has a three second timer to prevent overwhelming Reddit's server. This is a raw dataset that contains many columns. However, most of these were eliminated in data cleaning and exploratory data analysis. The key portion was the text posts. This dataset was merged with apple818.csv to create modeling.csv.


- modeling.csv: This dataset was a merger between the apple818.csv and google818.csv. It includes a time column called,'created_utc', an indicator of an Apple or Google called 'apple', the reddit post language called 'text', the Reddit title called 'title', the web address called'full link', and the number of comments called 'num_comments categories. These variables are discrete except 'num_comments.' This is the dataset used to model the data. It has 1,296 observations.

Presentation slides can be found [here](https://git.generalassemb.ly/vivekbavda/project_3/blob/master/BavdaNLPSlides.ipynb)

And this Readme.md

## Analysis and Conclusions

As the introduction explains, Mr. Amir Payeebaj of ANEC-NOC has hired Bavda Consulting to develop a model that will help ANEC-NOC decide whether to choose the Google or Apple customer service models.

The production model chosen is Random Forests for several reasons, most importantly, that the Cross Validation Score, Accuracy, Precision, Recall, and F1 Score were the highest for Random Forests above its competitors. 

The second recommendation is based off a polarity analysis that was done above. A polarity analysis is how positive or negative a group of text is. If one looks at the histogram of Google and Apple subreddits above, they nearly overlap each other. The measures of central tendency, meaning mean and median, are relatively close. Given this similarity, it may be that both Apple and Google are good models to follow. Perhaps combining their strategies might be the best for your company.

The third recommendation is that instead of trying to see whether Apple or Google have a better model, focus on your customers. It may be that Apple is good for its customers, and Google is good for its customers. Finding out what your company's customers like may be key to determining whom you should imitate. Using the Random Forests model developed, Logistic Regression model in combination, or all three models averaged, enter you company's subreddit posts and see whether the model predicts Google or Apple. By identifying your customers' needs and desires, this model could guide you to which company to imitate. Moreover, you can identify other subreddits that contain customers you would like to seek. Use their subreddit posts as the independent variable to determine whether Google or Apple is better for you.
