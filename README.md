# data-512-final-project
Final Project for Data:512 | University of Washington 

## A3: Final project plan
## Niharika Sharma

## Movies Recommender System using tradition approaches

### Project Proposal
In this project, we will build 4 different recommender system approaches based on different ideas and algorithms which would give us personalized results, the way Amazon and Netflix do it. The motivation behind this idea is that advertisements biases the recommendation on platforms like Amazon/ Netflix, IMDb, TMDb, etc. Hence, using the traditional approaches, we will build an unbiased recommender system to give a personalized recommendation to users.

### Data 
We have taken the dataset from Kaggle datasets - https://www.kaggle.com/rounakbanik/the-movies-dataset. The dataset consists of the following files:

movies_metadata.csv:  Contains information on 45,000 movies featured in the Full MovieLens dataset[7]. 
Fields in movies_metadata.csv include:
adult 
belongs_to_collection 
budget  
genres  
homepage 
id  
imdb_id  
original_language  
original_title 
overview 
popularity 
poster_path 
production_companies 
production_countries 
release_date 
revenue 
runtime 
spoken_languages 
status 
tagline 
title 
video 
vote_average 
vote_count 

keywords.csv: Consists the movie plot keywords for our MovieLens movies. 
Fields in keywords.csv include:
Id 
Keywords 

credits.csv: Contains Cast and Crew Information. 
Fields in credits.csv include:
Cast 
Crew 
Id 

links_small.csv: Contains the TMDB and IMDB IDs of a small subset of 9,000 movies of the Full Dataset.
Fields in links_small.csv include:
movieId 
imdbId 
tmdbId 

ratings_small.csv: Consist of rating for movies by anonymous users. The subset of 100,000 ratings from 700 users on 9,000 movies.
Fields in ratings_small.csv include:
userId 
movieId 
rating  
timestamp 

Released Under CC0: Public Domain 
License link: https://creativecommons.org/publicdomain/zero/1.0/


### Introduction

What are Recommender Systems?
Recommender Systems are widely used and have a variety of definitions. For instance,
1. A recommender system or a recommendation system (sometimes replacing "system" with a synonym such as platform or engine) is a subclass of information filtering system that seeks to predict the "rating" or "preference" that a user would give to an item. [1]  
2. Recommendation engines are the software that suggests what we should watch or read or listen to next. They help us deal with the millions of choices the Web offers. [2] 
3. Recommender Systems (RSs) are software tools and techniques providing suggestions for items to be of use to a user. [3] 
4. A recommender system is a technology that is deployed in the environment where items (products, movies, events, articles) are to be recommended to users (customers, visitors, app users, readers) or the opposite. [4] 
5. Recommender systems are systems that help users discover items they may like. [5]

For build a recommender system, there are multiple methods and approaches that we can use: 

Approach 1: Recommending the most popular items. This approach works well because there is a division by category and users can look category which interests them the most. Also, sometimes there are limited options, and these types of approaches work best on filtered data-set.

Approach 2: Content-based algorithms: Content-based recommender systems concentrate on the characteristics of the items and give recommendations based on the similarity between them, that is if you like an item then you will also like a “similar” item. For a movie recommender system, the features could be genre, average rating, tag keywords, number of users rating the movie, importance of the tag keyword, etc.

Approach 3: Collaborative filtering algorithms: Collaborative filtering is an Unsupervised Learning algorithm which produces recommendations based on the knowledge of user’ attitude to items, that is it uses the “wisdom of the crowd” and "past behavior" to recommend items. For instance, if Alex likes item A, B, C and Becca like B, C, D then they have similar interests and Alex should like item D and Becca should like item A. Companies like Netflix, Amazon,
use such methods extensively to provide rich recommendations to users. For such approaches, we retrieve all the data from the database. 
Such methods deal with the data sparsity, information overload, and cold start problem. Data sparsity arises from the phenomenon that users in general rate only a limited number of items and cold start refers to the difficulty in bootstrapping the Recommender Systems for new users or new items. 
There are two types of Collaborative filtering algorithms:
1. Item-item collaborative filtering - In the item-based approach a rating (u,i), from user u for item i, is produced by looking at the set of items similar to i (interaction similarity), then the ratings by u of similar items are combined into a predicted rating.[4]

2. User-user collaborative filtering - In the user-based approach, for user u, a score for an unrated item is produced by combining the ratings of users similar to u. [4]

Approach 4: There are other simpler algorithms, like co-occurrence matrix, market basket analysis, which work on the combinations of products without much rich algorithmic computation. These algorithms don't need much data; we can easily do the calculations using two columns - userId and movieId to get a similarity matrix. 

Approach 5: Hybrid Approach -  The amalgamation of Collaborative filtering and content-based approach is called a hybrid approach. It is very powerful technique as it takes advantages from both the approaches and eliminates the disadvantages like the cold-start problem, data sparsity. 
 
Methodology (what you will do with the data (e.g. statistical analysis, train a model))
1. Data Cleaning
    Rounding the Data
    Normalizing Ratings

2. Feature Engineering

3. Model training and testing
    We will deploy 4 approaches:
    1. Simple Recommender,
    2. Content-Based Recommender,
    3. Collaborative Filtering, and
    4. Hybrid Engine
    For measuring the similarity, we will use the following measures:
    1. Jaccard Distance, 
    2. Cosine Distance, or
    3. Pearson Correlation

### Expected Outcome (what results you expect or intend)

In this project, I will build 4 different recommender engines based on different ideas and algorithms which would give us personalized results, the way Amazon and Netflix does. They are as follows:
Simple Recommender: Using experimental designing techniques and filtering build movie charts by genre, performance, longest run time and other features.
Content-Based Recommender: Using movies textual, categorical and nominal metadata like taglines, cast, crew, genre, and keywords will predict similar movies. 
Collaborative Filtering: Using, either item-item CF or user-user CF built a similarity matrix for predicting the movie ratings by users.
Hybrid Engine: Combining the content and collaborative filtering approach will build an engine that will give movie suggestions to users based on the predicted ratings internally calculated for that user. 

Also, taking into consideration the Reproducibility in recommender system research, I will try to keep the features flexible to other datasets as well, so that the same approach could be applied to another movie recommender dataset. 

### Relevance of the project (why your project is interesting or important (and to whom, besides yourself))
The key reason why many big companies seem to care about recommender systems is money as they generate significant engagement and revenue. But, Advertisements biases the recommendation on platforms like Amazon, Netflix, IMDB, TMDB, Spotify etc. Hence, using the traditional approaches, we will build an unbiased recommender system for people to select movies. 
Also, building a recommender system is a true data science problem. It is a true representation and intersection between software engineering, machine learning, and statistics as building it requires all these skills. 

### References
1. https://en.wikipedia.org/wiki/Recommender_system
2.  "Facebook, Pandora Lead Rise of Recommendation Engines - TIME". TIME.com. 27 May 2010. Retrieved 1 June 2015.
3.  Francesco Ricci and Lior Rokach and Bracha Shapira, Introduction to Recommender Systems Handbook, Recommender Systems Handbook, Springer, 2011, pp. 1-35
4. https://medium.com/recombee-blog/recommender-systems-explained-d98e8221f468
5. https://yanirseroussi.com/2015/10/02/the-wonderful-world-of-recommender-systems/
6. https://www.kaggle.com/rounakbanik/the-movies-dataset
7. F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1â€“19:19. https://doi.org/10.1145/2827872



