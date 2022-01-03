# Amazon_Review-Sentiment
ML project on classifying Amazon Reviews as positive or negative

This is a sentiment analysis problem of training the machine in detecting positive or negative reviews.
In this project we will use classic ML as well as DL algorithms such as CNN and LSTM

Steps on completing the proeject. 
1) EDA analysis
    -It is determined that this is an imbalanced dataset, 94% of the data supports positive reviews.
2) We will convert the reviews to TFIDF but first we will clean the data by:
   - aplying lowercase
   - tokenizing the words in each sentence using RegexpTokenizer
   - remove stop words
   - Lemmatizing the words to its root using WordNetLemmatizer
   - joining the tokenized words back into sentences
   - Applying TfidfVectorizer on the sentecences with bigram and trigram ngram range.
3) Used Naive Bayes classifier on the imbalanced vectorized dataset to see how it performs. As predicted performance was bad in precision and recall.
4) Used SMOTE sampling technique to oversample the minority class
5) Re-ran the Multinomial Naive Bayes to look for improvements. As predicted oversampling improved precision recall and overall accuracy
6) Tried other Ensemble techniques like random forest and XGBoost   
   - optimized hyperparameter with random Forest and XGBoost by adding class weith balance to Random Forest and adding regularization to XGBoost
   - Used GridSearchCV to optimize SVM classifier
7) Assigned a sentiment score using TextBlob to segment each sentance with polarity and subjectivity
8) Re-ran ML algorithms to observe for results using the new Textblob feature
9) Used CNN to perform sentiment analysis, to do this we have to:
   - determine the total number of words used, the vocabulary size and the max sentence length. Using this we will create our image representation of the training sentences, padding any sentences shorter than the sentence with the maximum length
   - in our CNN we will regularization such as dropout 
10) We will use LSTM as well as LSTM with GRU to see model performance 
