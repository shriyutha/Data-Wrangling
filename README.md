# Data-Wrangling

WRANGLE AND ANALYZE DATA:

INTRODUCTION:

    The dataset that I will be wrangling (and analyzing and visualizing) is WeRateDogs, tweet archive of Tweeter account using python (and it's libraries).

    And will document wrangling efforts in Jupyter Notebook.

    The WeRateDogs is a Tweeter account, that rates people's dogs with a humorous comment about the dog.

    These ratings almost have a denominator of 10.

    The numerators always greater than 10. Like 11/10, 15/10, etc...

    Because "they are good dogs Brent."  

    WeRateDogs has over 4 million followers and recived international media coverage.

    WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for us to use in this project.

    This archive contains basic tweet data (tweet ID, timestamp, text, source, expanded_urls, name, etc...) for all 5000+ of their tweet as they stood on Auguest 1, 2017.   

    The main goal is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analysis and visualizations.

    Need to do addtional gathering, then assesing and cleaning for worthy analysis and visualizations.

THE DATA :

ENHANCED TWITTER ARCHIVE:

The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything.

One column the archive does contain though: each tweet's text, which I used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." 

We manually downloaded this file manually by clicking the following link: twitter_archive_enhanced.csv
Additional Data via the Twitter API:

1. Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable column omissions. 
2. Fortunately, this additional data can be gathered by anyone from Twitter's API.
3. Well, "anyone" who has access to data for the 3000 most recent tweets, at least. Because we have the WeRateDogs Twitter archive and specifically the tweet IDs within it, can gather this data for all 5000+.
4. And we are going to query Twitter's API to gather this valuable data.
IMAGE PREDICTIONS FILE:

The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network.

This file (image_predictions.tsv) hosted on Udacity's servers and we downloaded it programmatically using python Requests library on the following (URL)

url = https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)

Key Points :

Key points to keep in mind when data wrangling for this project:

We only want original ratings (no retweets) that have images.
Though there are 5000+ tweets in the dataset, not all are dog ratings and some are retweets.
Assessing and cleaning the entire dataset completely would require a lot of time, and is not necessary to practice and demonstrate our skills in data wrangling.
Therefore, the requirements of this project are only to assess and clean at least 8 quality issues and at least 2 tidiness issues in this dataset.
Cleaning includes merging individual pieces of data according to the rules of tidy data.
The fact that the rating numerators are greater than the denominators does not need to be cleaned.
his unique rating system is a big part of the popularity of WeRateDogs.
Do not need to gather the tweets beyond August 1st, 2017.
Twitter API:

In this project, we will be using Tweepy to query Twitter's API for additional data beyond the data included in the WeRateDogs Twitter archive. 

This additional data will include retweet count and favorite count.

Some APIs are completely open, like MediaWiki (accessed via the wptools library). Others require authentication. 

The Twitter API is one that requires users to be authorized to use it. This means that before we can run our API querying code, you need to set up our own Twitter application. 
