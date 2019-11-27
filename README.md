# NLP - Insincere Questions Classificaion
This is a capstone project for natural language processing specialization. In this project I've demonstrated usage of important concepts and technologies such as:
* __Structured and repeatable process for Data Science projects__
    * Initial Data Exploration
    * Extract, Transform, Load
    * Feature Creation
    * Model Definition
    * Model Training
    * Model Evaluation
    * Model Deployment

* python, pandas, seaborn, ntkl, sklearn, keras.

Work is structured in three notebooks. First focues on EDA and ETL, second and third focused on modeling with classical ML and Neural networks.
1) __EDA - Explorative Data Analysis__
    * Demonstrate graphical and numerical techniques to uncover the structure of the data.
        * Which variables suggest interesting relationships?
        * Which observations are unusual?
        * Analysis of the features
    * Frequency plots, ngrams, wordclouds, ...
    
2) __Using conventional methods in NLP setup__
    * Conventional preprocessing and data preparation for NLP 
        * CountVectorizer
        * TFIDF
    * Evaluating conventional Machine Learning Algorithms
        * LogisticRegression
        * Random Forest
        * XGBoost
        * Making predictions from ensemble, Voting Classifier

3) __Using LSTM neural network with word embeddings__ 
     * Ensuring maximal text coverage with embeddings
     * Discussion of LSTM architecture
     * Training LSTM Neural Networks
     * Evaluating performance

## Problem Description
This is classification problem of predicting whether a question asked on Quora is sincere or not.

An insincere question is defined as a question intended to make a statement rather than look for helpful answers. Some characteristics that can signify that a question is insincere:

* Has a non-neutral tone
    * Has an exaggerated tone to underscore a point about a group of people
    * Is rhetorical and meant to imply a statement about a group of people
* Is disparaging or inflammatory
    * Suggests a discriminatory idea against a protected class of people, or seeks confirmation of a stereotype
    * Makes disparaging attacks/insults against a specific person or group of people
    * Based on an outlandish premise about a group of people
    * Disparages against a characteristic that is not fixable and not measurable
* Isn't grounded in reality
    * Based on false information, or contains absurd assumptions
    * Uses sexual content (incest, bestiality, pedophilia) for shock value, and not to seek genuine answers

The training data includes the question that was asked, and whether it was identified as insincere (`target = 1`). The ground-truth labels contain some amount of noise: they are not guaranteed to be perfect.

Note that the distribution of questions in the dataset should not be taken to be representative of the distribution of questions asked on Quora. This is, in part, because of the combination of sampling procedures and sanitization measures that have been applied to the final dataset.

## Data fields
* qid - unique question identifier
* question_text - question text
* target - a question labeled "insincere" has a value of `1`, otherwise `0`

## Embeddings
External data sources are not allowed for this competition. We are, though, providing a number of word embeddings along with the dataset that can be used in the models. These are as follows:

* GoogleNews-vectors-negative300 - https://code.google.com/archive/p/word2vec/
* glove.840B.300d - https://nlp.stanford.edu/projects/glove/
* paragram_300_sl999 - https://cogcomp.org/page/resource_view/106
* wiki-news-300d-1M - https://fasttext.cc/docs/en/english-vectors.html