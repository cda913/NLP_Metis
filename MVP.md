# Minimum Viable Product

### Background
The fans of a movie podcast ("Blank Check with Griffin & David") have created a subreddit about the podcast. Can we find unusual topics across threads in the subreddit?

### MVP
Data is from [here](https://www.reddit.com/r/blankies/), downloaded on November 5th, 2021. Posts vary from single sentences to in-depth comments. Posts with rating 18 or higher were selected, giving 2070 posts

After cleaning the data and vectorizing using Tfidf, I ran a 20-component LDA model. Visualization of the 20-component data showed there are two separate categories; the other 18 categories lay on top of each other in 2D space. I ran a 3-component LDA model, and below is a visualization:

<img src="https://github.com/cda913/NLP_Metis/blob/main/pyLDAvis_three_cat_Nov8.png" width="400" height="200" />

From "Most Relevant Terms", topic 1 appears to be about the show in general, topic 2 appears to be about a specific yearly activity the show does, and topic 3 appears to be about everything else. 

However, if we return to the 20-topic graph, there is one topic of interest in the overlapping topics. Given the "Most Relevant Terms, it appears to be about a recurring segment on the show:

<img src="https://github.com/cda913/NLP_Metis/blob/main/pyLDAvis_possibleOther_Nov7.png" width="400" height="200" />

I will be working to find other interesting results like this.

### To Do
- Add more stop words to data cleaning, for example "movie" and "film".
- Reduce dimensionality.
- Try other vectorization methods.
- Look into categories more closely.
