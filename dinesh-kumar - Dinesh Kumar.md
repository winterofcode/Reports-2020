# Developer - Winter of Code 2020
# Dinesh Kumar
### DSE IEM : Text Sentiment Analysis

This project is based on Text Sentiment Analysis.In this project if we put text as input it gives output in three category are postive, negative and neutral text and gives keyword and summary with respective input.

I am [Dinesh Kumar](https://github.com/Dineshkumar536), an undergraduate student from NIET, Noida, as part of [Winter of Code](https://winterofcode.com/).

This project was mentored by - [Farhan Hai Khan](https://github.com/khanfarhan10) and [Tannistha Pal](https://github.com/paltannistha). The project had constant guidance from [Farhan Hai Khan](https://github.com/khanfarhan10) .

# Contributions
## 1.Selection a Proper Dataset
* Getting proper data for training models suitable to our requirements is important.
* I have searched a lot of dataset like twitter analysis data and many more but at last i finalised **Amazon Fine Food Review** .
* I have choosed this dataset because it includes rating from **0-5 scores** for every individual review.
* The data span a period of more than 10 years, including all **~500,000 reviews** up to October 2012.
* It contains **huge** dataset due to this i have choosen this dataset for my project.


## 2. Data Preprocessing on dataset
* Before we move to train our model we have to do preprocessing so that we can **remove unwanted data**.
* So here in my dataset there are various columns of different values but for my project i have selected only **scores , id and reviews text** column for my project.
* after that there is score given 0-5 for reviews so i divided that into 3 categories **negative(score>3),Positive(score>3),neutral(score==3)**.
* after that i have checked that if any **duplicate values** are there than i have seen that there are duplicates values , I removed all duplicated value.
* Then i removed **html tags**, **special character** and **Tokenize** the reviews into word tokens.
* After that i split the review into words and then check if these words are in the **stop words** if so we will remove them, if not we will join.

## 3.Featurisation , Tf-idf
* Now we have splitted my cleaned dataset into **train and test set** to work on that and build a gentle model.
* Then i featurised my dataset on tf-idf vectorizer and fit it as **tfidf_model.fit(reviews_train,sentiment_train)**.
* Then i transform it on train reviews as **reviews_train_tfidf=tfidf_model.transform(reviews_train)**.
* Then i used **WordCloud** to see **top 10 words** by importing Wordcloud in my model.


## 4.Model Selection
* Model selection is very **key point** to make your project best in term of accuracy and precission.
* after applying **EDA** on dataset i tried **three algorithms** to train my model for better prediction.
* These are 3 algorithms :- **Logistic Regression, Naive Bayes and Decision tree**.
* From these three i have figureout one algorithm which will fit to my model.
* So on the basis of **parameters** and **accuracy** i choosed Naive Bayes for my model to train my model on it.


## 5.Model Deployement
* For pre-check my model **frontend and backend** i deployed it on my local server, and it working efficiently and precisely.
* I have added feature of **prediction of sentiment** , **keywords extraction and showing** , **Polarity and Subjectivity** and **Summary**. these are some features which will comes up when we put sone text in my frontend and gives output after processing in backend.
* link of my web app
https://sentimentproject.herokuapp.com/

## 6.Future Scope
* Working in the project of **Text Sentiment Analysis** not only we got more application in machine learning but we also got more intents towards different arean of NLP(Natural Language Processing).

## 7.Overall Experience
* It was great exprience for me to got into **Open Source** culture through this great program and I would love to encorage more students to do this program in future.

Here are some of [my PRs](https://github.com/khanfarhan10/TextSentimentAnalysis/blob/main/Final_Report.md)
