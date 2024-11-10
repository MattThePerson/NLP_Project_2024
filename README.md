# Recipe Recommender System - NLP Project 18 (2024)

Project by Matt Stirling & Pau Roca


## Notebooks

* **matti_notebook.ipynb**
    * (Tasks 1-2) Exploration and User Profiles
    * (Tasks 5-7) Similarity calculations \
    FILES CREATED:
    * **User_Data.csv**
    * **Recipe_Reviews.csv**
* **pau_notebook.ipynb**
    * (Tasks 3-4) Sentiment analysis
    * (Tasks 8-9) Clustering
* **recommender_contentBased.ipynb** 
    * (Task 10) Recommender system \
    FILES CREATED:
    * **User_Data_Train.csv**
    * **User_Data_Test.csv**


## How to run

* Install python dependencies in requirements.txt
* Visit https://www.kaggle.com/code/ngohoantamhuy/food-recommendation-systems and download the files: 
    * **RAW_interactions.csv**
    * **RAW_recipes.csv**
* Place the files in a folder called 'dataset' (not tracked by git)


## Description of Recommender Systems


1. TF-IDF (content-based)
    - **(item profiles)** Generate item profiles from combined TF-IDF matrix
    - **(user profiles)** Generate user profiles by getting mean of weighted recipe embeddings
    - **(user-item SIM)** Cosine sim between user and recipe embeddings to find n recommended items


2. Collaborative filtering
    - **(user profiles)** Use user-item rating matrix as feature space
    - **(user-user SIM)** Find users with similar rating profiles (CC) and recommend n recipes sorted by *(user_rating x similarity)* and not rated by user


3. DistilBERT (content-based)
    - **(item profiles)** Get recipe embeddings using DistilBERT model
    - **(user profiles)** Get user embeddings by getting mean of weighted recipe embeddings for rated recipes
    - **(user-item SIM)** Cosine sim between user and recipe embeddings to find n recommended items
