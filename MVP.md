# Minimum Viable Product

### Background
The fans of a movie podcast ("Blank Check with Griffin & David") have created a subreddit about the podcast. Can we find topics across threads in the subreddit that might help direct the podcast in the future?

### MVP
Data is from [here](https://www.reddit.com/r/blankies/). Posts vary from simple memes to in depth comments.

I downloaded all comments with a rating of 18 or higher, which gave me 2070 posts. I cleaned the text, tokenized the text as single word tokens, and removed stop words, which left me with . I ran a Tfidf model on the 
