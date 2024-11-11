# NLP Project 18 - Recipe Recommender System (2024)

Natural Language Processing class of 2024 (University of Oulu)\
Project by Matt Stirling & Pau Roca.


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
    * DistilBERT testing
* **recommender_contentBased.ipynb** 
    * (Task 10) Recommender system \
    FILES CREATED:
    * **User_Data_Train.csv**
    * **User_Data_Test.csv**
    * **recommendations**
* **recommender_collaborativeFiltering.ipynb**
    * (Task 11) Collaborative filtering \
    FILES CREATED:
    * **recommendations**
* **recommender_DistilBERT.ipynb**
    * (Task 14) DistilBERT embeddings using recommender \
    FILES CREATED:
    * **recommendations**
* **recommender_evaluations.ipynb**
    * (Tasks 10, 11 & 14) Evaluations of the different models


## How to run

* Install python dependencies in requirements.txt
* Have means to run Jupyter Notebooks
* Visit https://www.kaggle.com/code/ngohoantamhuy/food-recommendation-systems and download the files: 
    * **RAW_interactions.csv**
    * **RAW_recipes.csv**
* Place the files in a folder called 'dataset' (not tracked by git)
* Run **matti_notebook.ipynb** first to generate necessary data


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
