# Steam-Game-Review-Analysis-NLP-

## About the dataset ##
Steam is the world's most popular PC Gaming hub, with over 6,000 games and a community of millions of gamers.

This dataset contains about reviews of Games on Steam, scraped from the Steam API. Each review determines whether or not the user recommends to buy this game.
There are 4 csv files in the current version of the dataset.The train.csv file has over 17k reviews of different games.We have only used the train dataset to visualize and build our models.

The various columns in the dataset are :

1. Title : Game title
2. Year : Year the review was written
3. User_Review : The user review on steam platform
4. User_Suggestion : A binary variable which represents whether a user suggests whehter you should buy the game or not. (0 - Not suggested to buy 1 - Suggested to buy)
5. Review_id : Id of the reviewer

Source:
This dataset was taken from kaggle.Find the dataset at the link below and click on Download

 <https://www.kaggle.com/whoiskk/steam-game-reviews>
 
 
## Objective: ##
Sentiment analysis is the interpretation and classification of emotions (positive, negative) within text data using text analysis techniques. We perform sentiment analysis to this dataset and train our models to predict whether the user recommends others to buy the game or not.This is represented as 0 or 1.

## Tasks ##

### 1. Data Visualization ###
Graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

Here is the direct colab notebook link:

https://colab.research.google.com/drive/136Qk6TPmAFlLTS2UjVOY3LFu9Adrb1RF#scrollTo=MCqAyaoWc-rh

### 2.Data Pre-processing ###
The data can have many irrelevant and missing parts. To handle this part, data cleaning is done. It involves handling of missing data, noisy data etc.
The cleaned dataset is uploaded back to drive for further use

Here is the direct colab notebook link:

https://colab.research.google.com/drive/1UN3kvIb1svNQ5zVBrtthPLbalCeNWuh6#scrollTo=lwz2jPNU1U22

### 3. Models used to Train Data and results ###


#### 1.  Word Embedding ####

Here is the direct colab notebook link:

https://colab.research.google.com/drive/1UN3kvIb1svNQ5zVBrtthPLbalCeNWuh6#scrollTo=R6dza2lN1z86

Train accuracy | Validation accuracy
------------- | -------------
83.85% | 84.23%


#### 2. Vectorization (CountVect and TDIDF) ####

Here is the direct colab notebook link:

https://colab.research.google.com/drive/1fZjeGvoKJ7PN3iKY-aHebx2Wq4K5Lxak#scrollTo=IFamrNcwkLz2

Count Vectorization

    1. Logistic Regression
Train accuracy | Validation accuracy
------------- | -------------
98.61% | 83.16%

    2. KNN
Train accuracy | Validation accuracy
------------- | -------------
74.91% | 63.40%

Tfidf Vectorization

Train accuracy | Validation accuracy
------------- | -------------
84.09% | 81.10%

 
## Conclusion ##

Model | Train accuracy | Validation accuracy 
------------- | ------------- | -------------
Count Vectorization LR| 98.61% | 83.16%
Count Vectorization KNN| 74.91% | 63.40%
Tfidf Vectorization | 84.09% | 81.10%
Word Embedding | 83.85% | 84.23%

1. It is observed that NeuralNetworks using Word Embeddings performs better than any other model.It represents words as semantically-meaningful dense real-valued vectors. This overcomes many of the problems that simple one-hot vector encodings have. Most importantly, embeddings boost generalisation and performance for pretty much any NLP problem
2. We can see that our accuracy has increased from 63.4% (CountVect -KNN) to 81.10% (TF-IDF Vect) and remains almost same as (CountVect- LogReg) 83.16%
3. Training the model by vectorizing the texts using CountVectorizer() performs better than using TfidfVectorizer().

Word Embedding performs the best!


### Instructions to go through the notebooks

You can download the .ipynb files on your system using Download or Clone button and view them in the following order

1. Data_Visualization.ipynb
2. Steam_Game_Review_Analysis_Word_Embedding_in_Keras_ (1).ipynb has Data-preprocessing as well as code for WordEmbedding
3. SteamGame_Review_Analysis_Vectorization.ipynb has code for both Count Vectorization and Tfidf Vectorization

Thank you!
