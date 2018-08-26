

# Recommender System

If you have a Netflix account, you must be always wondering 

*What movie should I watch?* 

You may already notice online streaming companies, like Netflix and Hulu, have taken care of this and provided personalized recommendations every time you log in. Today, recommender systems have been used everywhere from music (Spotify), books (Amazon), jobs (LinkedIn) to search engine results (Google). 

In this project, we utilize model-based collaborative filtering and [MovieLens](https://grouplens.org/datasets/movielens/) dataset build a prototype movie recommendation system.  An interactive user interface can be implemented with Jupyter notebook.

 <img src="./IMG/img1.png" width="400">

### Collaborative filtering

Collborative filtering is one of the classical approaches in recommender system and based on the past user (customers) behavior on the items (products). It analyzes the similiarity of item preference (rating or purchase history). Most interestingly, it does not depend on the item content details but focus on extract the extract the collaborative behavior. This makes collaborative filtering a general methodogy and can be simply applied to any kinds of products. 

There are two types:

1. User-based collaborative filtering
2. Item-based collaborative filtering
3. Model-based collaborative filtering

The first two are also called memory-based collaborative filtering and rely on user-to-user and item-to-item similarity to provide recommendatin. In this project, we use model-based collaborative filtering (CF), which is more tied to machine learning concept. 

### Model-based CF & matrix factorization

The dataset in recommender system is usually a large sparse matrix of size M x N for N items and N users. Since the items every user can afford to rate/purchase/browse are much less than N, majority of the matrix elements are zero. Assuming there is a hidden structure governing the item-user behavior, we can project  this matrix to a lower dimention of k by matrix factorizatoin. The low dimensionality k can be interpreted as clusters or categories for certain groups of users or items. Practically, we want o factorize M x N matrix to one M x k and one k x N matrices. The former represents a product feature matrix and the latter represents  user feature matrix. 