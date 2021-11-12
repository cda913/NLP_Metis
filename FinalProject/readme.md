# Finding Topics in a Subreddit

### Abstract
Fans of a movie/comedy podcast (“Blank Check with Griffin & David”) founded a subreddit about the podcast in 2016. Do the members of the subreddit discuss other topics besides the podcast? I looked at the entire subreddit through November 2, 2021, and used several unsupervised learning techniques to find topics. Results were mixed, with different tokenizers producing different topics. However, one topic showed up in all techniques: a yearly interactive activity from the podcast. 
### Design
“Blank Check with Griffin & David” is a movie/comedy podcast that discusses one movie per episode, in “miniseries” focused around directors. Fans of the show created a [subreddit](https://www.reddit.com/r/blankies/) in 2016. I wanted to know if members discussed any other topics besides the podcast. I used unsupervised clustering techniques to determine the answer. 
### Data
All posts that had a minimum of upvote score of 18 were downloaded from Reddit on November 2, 2021. Posts ranged from single sentences to paragraph-long, in-depth comments. There were 2070 posts in total.
### Algorithms
I cleaned the text to remove as many stop words as possible. I ran two separate tokenizers on the text. After tokenizing, I tested three classifiers each on the differently tokenized data. All combinations found different topics, but there were some overlaps. 

All combinations found a general conversation topic. Four of the six combinations of tokenizer and learner found a topic focused on a yearly interactive activity run by the podcast: non-basketball “March Madness” where the fans vote to choose a director for the podcast to discuss. 

With CountVectorizer as a tokenizer, all of the learning techniques found a topic about YouTube and a topic about Legos. 

When the more stringent TfidfVectorizer was used to tokenize, none of the learners found the YouTube or the Lego topic. However, LSA did find a topic about the movie Gemini Man.
### Tools
- psaw for downloading data
- Numpy and pandas for data manipulation
- spaCy for text cleaning
- CountVectorizer and TfidfVectorizer for vectorization
- TruncatedSVD, LDA, and NMF for unsupervised learning
- pyLDAvis, WordCloud, and Excel for visualizations 
### Communication
PowerPoint presentation

