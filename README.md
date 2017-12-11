# data-512-final-project
Final Project for Data - 512 | University of Washington   
Niharika Sharma

### Recommender System

### Abstract
From our research project, we tried to build 2 recommendation algorithms from scratch and tried to answer two hypothesis -
1. Compare the recommender personality of content-based and collaborative filtering Recommender System

2. Why should a user trust that the algorithm understands who they are, what they like and what they are doing?

By doing this project we compared and predicted the subjective characteristics of recommendation algorithm. We find that the recommendations from collaborative filtering approach are quite diverse and fresh, whereas the recommendations from content-based approach are quite the opposite. It depends on the requirement of the users and what kind of recommendations they would like. Moreover, whatever recommendation we provide to the user, the two key important factors to keep in mind is awareness and explanation of the recommendations. Let the users be aware of how we are adapting to their tastes and make it clear that we are not recommending movies/items because it suits our business needs, but because it matches the information we have from them: their explicit taste preferences and ratings, their viewing history.
In conclusion, recommender systems need a deeper understanding of users and their information seeking tasks to be able to generate better recommendations[10]. 

### Data 
We have taken the dataset from Kaggle datasets - https://www.kaggle.com/rounakbanik/the-movies-dataset. The dataset consists of multiple files but we are using the following files:

movies_metadata.csv:  Contains information on 45,000 movies featured in the Full MovieLens dataset[7]. 
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

links_small.csv: Contains the TMDB and IMDB IDs of a small subset of 9,000 movies of the Full Dataset.
Fields in links_small.csv include:  
movieId   
imdbId   
tmdbId   
 
ratings_small.csv: Consist of rating for movies by anonymous users. The subset of 100,000 ratings from 700 users on 9,000 movies.
Fields in ratings_small.csv include:  
userId   
movieId   
rating    
timestamp   

### License for the data
Released Under CC0: Public Domain 
License link: https://creativecommons.org/publicdomain/zero/1.0/


### Introduction and background on Recommendation algorithms - 

What are Recommender Systems?
Recommender Systems are widely used and have a variety of definitions. For instance,
1. A recommender system is a subclass of information filtering system that seeks to predict the "rating" or "preference" that a user would give to an item. [1]  
2. Recommendation engines are the software that suggests what we should watch or read or listen to next. They help us deal with the millions of choices the Web offers. [2] 
3. Recommender Systems (RSs) are software tools and techniques providing suggestions for items to be of use to a user. [3] 
4. Recommender systems are systems that help users discover items they may like. [5]

For build a recommender system, there are multiple methods and approaches that we can use: 

Approach 1: Recommending the most popular items. This approach works well because there is a division by category and users can look category which interests them the most. Also, sometimes there are limited options, and these types of approaches work best on filtered data-set.

Approach 2: Content-based algorithms: Content-based recommender systems concentrate on the characteristics of the items and give recommendations based on the similarity between them, that is if you like an item then you will also like a “similar” item. For a movie recommender system, the features could be genre, average rating, tag keywords, number of users rating the movie, importance of the tag keyword, etc.

Approach 3: Collaborative filtering algorithms: Collaborative filtering is an Unsupervised Learning algorithm which produces recommendations based on the knowledge of user’ attitude to items, that is it uses the “wisdom of the crowd” and "past behavior" to recommend items. For instance, if Alex likes item A, B, C and Becca like B, C, D then they have similar interests and Alex should like item D and Becca should like item A. Companies like Netflix, Amazon,
use such methods extensively to provide rich recommendations to users. For such approaches, we retrieve all the data from the database. 
Such methods deal with the data sparsity, information overload, and cold start problem. Data sparsity arises from the phenomenon that users in general rate only a limited number of items and cold start refers to the difficulty in bootstrapping the Recommender Systems for new users or new items. 
There are two types of Collaborative filtering algorithms:
1. Item-item collaborative filtering - In the item-based approach a rating (u, i), from user u for item i, is produced by looking at the set of items similar to i (interaction similarity), then the ratings by u of similar items are combined into a predicted rating.[4]

2. User-user collaborative filtering - In the user-based approach, for user u, a score for an unrated item is produced by combining the ratings of users similar to u. [4]

Approach 4: There are other simpler algorithms, like co-occurrence matrix, market basket analysis, which work on the combinations of products without much rich algorithmic computation. These algorithms don't need much data; we can easily do the calculations using two columns - userId and movieId to get a similarity matrix. 

Approach 5: Hybrid Approach -  The amalgamation of Collaborative filtering and content-based approach is called a hybrid approach. It is very powerful technique as it takes advantages of both the approaches and eliminates the disadvantages like the cold-start problem, data sparsity. 

### What can be expected in the Jupyter Notebook -

In this project, we have built 2 different recommender engines based on different ideas and algorithms which would give us personalized results. They are as follows:  
Content-Based Recommender: Using movies taglines and overview feature.   
Collaborative Filtering: Using, either item-item CF built a similarity matrix for predicting the movies for users.

The Jupyter notebook that contains both our written report, our code and findings related to the hypothesis mentioned in the abstract.

Also, taking into consideration the Reproducibility in recommender system research, I have tried to keep the features and variables flexible, so that the same approach could be applied to another movie recommender dataset.  

### Relevance of the project (why our project is interesting or important (and to whom, besides ourself))
The fundamental reason why many companies seem to care about recommender systems is for money and business as they generate significant user engagement and revenue. But, Advertisements biases the recommendation on platforms like Amazon, Netflix, IMDB, TMDB, Spotify etc. Hence, using the traditional approaches, we will build an unbiased recommender system for people to select movies.   
Building a recommender system is a true data science problem. It is a true representation and intersection between software engineering, machine learning, and statistics as building it requires all these skills. 


## Reproducibility 
For running and replicating the results and algorithm, install all the packages correctly as mentioned in the Jupyter Notebook and run the Jupyter Notebook.

You can use a larger dataset or a different dataset but make sure that the column name and column type remains the same. Any other change in the new data set might reduce the chances of reproducibility. 


## Known issues or special considerations with the data

Expected outcome and understanding of the results from the algorithms may differ person to person.

Change of dataset may make the whole research questionable as the findings we got can change if the dataset changes.

### References
1. https://en.wikipedia.org/wiki/Recommender_system
2.  "Facebook, Pandora Lead Rise of Recommendation Engines - TIME". TIME.com. 27 May 2010. Retrieved 1 June 2015.
3.  Francesco Ricci and Lior Rokach and Bracha Shapira, Introduction to Recommender Systems Handbook, Recommender Systems Handbook, Springer, 2011, pp. 1-35
4. https://medium.com/recombee-blog/recommender-systems-explained-d98e8221f468
5. https://yanirseroussi.com/2015/10/02/the-wonderful-world-of-recommender-systems/
6. https://www.kaggle.com/rounakbanik/the-movies-dataset
7. F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1â€“19:19. https://doi.org/10.1145/2827872
8. http://blog.manugarri.com/a-short-introduction-to-recommendation-systems/
9. http://blog.untrod.com/2016/06/simple-similar-products-recommendation-engine-in-python.html
10. Michael D. Ekstrand, F. Maxwell Harper, Martijn C. Willemsen, and Joseph A. Konstan. 2014. User perception of differences in recommender algorithms. In Proceedings of the 8th ACM Conference on Recommender systems (RecSys '14). ACM, New York, NY, USA, 161-168. DOI: https://doi.org/10.1145/2645710.2645737
11. Sean M. McNee, John Riedl, and Joseph A. Konstan. 2006. Making recommendations better: an analytic model for human-recommender interaction. In CHI '06 Extended Abstracts on Human Factors in Computing Systems (CHI EA '06). ACM, New York, NY, USA, 1103-1108. DOI=http://dx.doi.org/10.1145/1125451.1125660
12. Michael D. Ekstrand and Martijn C. Willemsen. 2016. Behaviorism is Not Enough: Better Recommendations through Listening to Users. In Proceedings of the 10th ACM Conference on Recommender Systems (RecSys '16). ACM, New York, NY, USA, 221-224. DOI: https://doi.org/10.1145/2959100.2959179
13. Xavier Amatriain and Justin Basilico. Netflix Recommendations: Beyond the 5 stars. Netflix Tech Blog, 2012.
14. Brian Whitman. How music recommendation works - and doesn't work. Variogram, 2012.
15. Bart P. Knijnenburg, Martijn C. Willemsen, Zeno Gantner, Hakan Soncu, and Chris Newell. 2012. Explaining the user experience of recommender systems. User Modeling and User-Adapted Interaction 22, 4-5 (October 2012), 441-504. DOI=http://dx.doi.org/10.1007/s11257-011-9118-4
16. Sean M. McNee, Nishikant Kapoor, and Joseph A. Konstan. 2006. Don't look stupid: avoiding pitfalls when recommending research papers. In Proceedings of the 2006 20th anniversary conference on Computer supported cooperative work (CSCW '06). ACM, New York, NY, USA, 171-180. DOI=http://dx.doi.org/10.1145/1180875.1180903


