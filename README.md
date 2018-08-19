This repository analyses the dataset from the famous social networking site Twitter.

Dataset Courtesy: Stanford University

This dataset is called Sentiment140. 

Link to the dataset
http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip 


More info on the dataset can be found from the link. http://help.sentiment140.com/for-students/

By looking at the description of the dataset from the link, the information on each field can be found.

0 — the polarity of the tweet (sentiment) (0 = negative, 2 = neutral, 4 = positive)

1 — the id of the tweet (2087)

2 — the date of the tweet (Sat May 16 23:58:44 UTC 2009)

3 — the query. If there is no query, then this value is NO_QUERY.

4 — the user that tweeted

5 — the text of the tweet

After taking a look at the dataset we conclude that:

1) Dataset has 1.6 million entries with no null entries.

2) Even though the dataset description mentioned neutral class, the training set has no neutral class.

3) 50% of the data is with negative label, and another 50% with positive label.

We must first start by dropping the columns we don't need for the purpose of sentiment analysis.

-> “id” column is unique ID for each tweet

-> “date” column is for date info for the tweet

-> “query_string” column indicates whether the tweet has been collected with any particular       
     query key word, but for this column, 100% of the entries are with value “NO_QUERY”

-> “user” column is the twitter handle name for the user who tweeted

I started by dropping the above listed columns.

#Data Preparation

As a way of sanity check, let’s look at the length of the string in text column in each entry.

#Data Dictionary

This my first draft of the dataset. It will be updated as we move on.

Now lets have a look at the boxplot of the data.

#Note

Here we have a strange observation, Twittter  has a character limit of 140 but there are many tweets that exceed this limit.