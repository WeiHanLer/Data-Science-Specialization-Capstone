# Data Science Specialization Capstone

## Overview

This is the **final** project in the data science capstone which completes the data science specialization course.

The objective of the project is to produce a Shiny app that is capable of predicting the next word that comes after the user's input of words. . The base [dataset][links] used to train the prediction model consists of texts from different sources: twitter, blogs and news articles. 
A milestone report on the completion of this project is also produced:http://rpubs.com/whyler12/CMP

More informaton on this course can be found [here][link], at the official John Hopkins University Data Science Capstone Coursera page. 


[link]:https://www.coursera.org/learn/data-science-project
[links]:https://d396qusza40orc.cloudfront.net/dsscapstone/dataset/Coursera-SwiftKey.zip

## Shiny App & Simple Presentation Deck
The prototype of the Word Prediction App and the submitted presentation deck can be accessed below:

#### [Word Prediction App](https://lerweihan.shinyapps.io/DataScienceFinalProject)
#### [Presentation Deck](http://rpubs.com/whyler12/FINAL) 

## Concept of the Text Prediction Model 

The idea behind the prediction model is the Katz Back-off algorithm. 

The aforementioned three documents are read into a corpus,cleaned and tokenisation is applied to produce N-grams, specifically Quadgrams,Trigrams, Bigrams and Unigram. 

When a user input is detected, the Quadgram is first used to predict the next word to occur in the phrase.
If no Quadgram is found, the Trigram is used instead to predict the output and then the Bigram. If there are still no results, the most frequently occuring single word is given as a last resort. The flow of the process is "backing-off" from the higher number n-grams to the lower ones.


