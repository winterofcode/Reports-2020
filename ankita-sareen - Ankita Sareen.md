# Developer - Winter of Code 2020
# Ankita Sareen
### DSC IEM : TextSentimentAnalysis
* **Project:** [TextSentimentAnalysis](https://github.com/khanfarhan10/TextSentimentAnalysis)



## Overview
## Contributions 
* ### Selection of proper Dataset 
Getting proper data for training models suitable to our requirements is important.Therefore, I picked up the well known "Amazon fine food reviews" dataset from the kaggle.

* ### Featurisation, EDA and Tf-idf
Using the seaborn library and wordcloud,tried to analyse the prediction column and the major words for the respective sentiment.
   * Tokenization
         In order to perform machine learning on text documents, I first need to turn these text content into numerical feature vectors that Scikit-Learn can use. 
   * Sparse Matrix
        I then transformed the document into a bag-of-words representation i.e matrix form. The result is stored in a sparse matrix i.e it has very few non zero elements.Rows represent the words in the document while columns represent the words in our training vocabulary.
    * Used TF IDF over bag of words.
        

* ### Model selection and n-gram modelling
 Of all the models tried, Logistic Regression works the best after vectorisation and n-gram modelling giving the accuracy of 93% and ROC_AUC score of 90% around which is pretty good model.

     
  Training Script: https://colab.research.google.com/drive/14ekbzUx0dcEkzMdwBAhbdf4fflz6lL4H?usp=sharing

  
* ### Deploy the model in flask 
Model was further integrated with flask and then deployed on heroku with further implementation of features such as summarisation.
 
* ### Built a Utility Tool for  Zip File Upload
Added the feature of zip file upload, from which then csv files are extracted and predictions are made from the model. Also added one more feature, a link from where you can download the csv of the prediction dataframe generated.

## New features 
Some of the new features were:

1. Summarisation 

2. Deployed webapp

3. Zip file upload feature

* Issues
    **Improve, Design & Optimize the NLP Models #3:** https://github.com/khanfarhan10/TextSentimentAnalysis/issues/3
     **Improve Utility Tools - Zip File Upload #4:**https://github.com/khanfarhan10/TextSentimentAnalysis/issues/4


* Here are some of my PRs.
      *Pull Requests:*
  * **Model Improvised:** https://github.com/khanfarhan10/TextSentimentAnalysis/pull/18
  * **Zip file upload #28:** https://github.com/khanfarhan10/TextSentimentAnalysis/pull/28
  * **Small changes to app.py #34:** https://github.com/khanfarhan10/TextSentimentAnalysis/pull/34

 
## Future scope
While working in the project of TextSentiment Analysis not only we got aware about more applications of NLP but we also got ideas about how to make the project more meaningful for the community around. There are so many new aspects that this project can take up. These are some of them:

1. Deploying the flask server onto google cloud , aws or azure.
2. Improving the current web application by using a robust frontend framework like react or angular.
3. Implementing features such as para phrasing etc for a multipurpose use by the community.

## Overall Experience
I had an enriching and exciting winter of 2020, working on this project under the Winter of Code program. I was glad to be mentored by Farhan (thanks for going through all my PRs!) and Tanishtha (who helped us with her vast knowledge in and around NLP). I express my sincere thanks to all my peers working as part of WoC.

Woc was a warm and unforgettable experience for me. Everytime I talk of Open Source, TextSentiment Analysis will be remembered fondly.
