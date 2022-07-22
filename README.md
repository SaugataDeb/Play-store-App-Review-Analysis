## SaugataDeb-Play_store_App_Review_Analysis

## Abstract:
Android is an operating system which has
Currently 2.8 billion users are active around the globe. In this project we will be doing analysis on Play Store App Review Data. With the development of android initially it was an operation system to be used in camera but when google acquired android in 2005. They started giving android as an operating system to smartphones in 2007 which was later going to dominate 1/3rd of the world's total population as what we are experiencing today. Android is basically an open source OS giving the developers an opportunity to develop applications in this data ridden world because of this it has become necessary for the data analytics professionals to analyze those data so to help companies realize how they can grow their business effectively in every aspect and learn the needs of the users for the betterment of their products and also help App developers how they can improve their products in different categories.

##  Problem Statement:
Data has been provided by ABC Advertising Pvt. Ltd.  to analyze the data for different App in different categories and help them satisfy their customers needs who possibly  
resides around the world. From these analyses they can understand the needs of their customers in different aspects of product development and it will help solve the problems with the market superiors. 
The main objective of this project is to deal with the data provided by the company and to analyze the data in every aspect possible so to help them match their idea and help them to convert new and retain old customers and make reasonable growth.
We have been provided with two datasets:
Play Store Data.csv
User Reviews.csv
## Play Store Data.csv column elements:-

1. App - Name of the Application
2. Category - Category of the Application
3. Rating - Rating given to the Application
4. Reviews - No of reviews given to the Application
5. Size - Size of the Application
6. Installs - No of downloads of the Application
7. Type - Free or Paid
8. Price - Price of the Application if it is paid
9. Content Rating-It is Age appropriate or Not
10. Genres - Type of Genre the Application belongs to
11.Last Updated - When the last time the Application is Updated
12. Current Ver - Current version of the Application
13. Android Version- Minimum Android version required to run the Application

## User Review.csv column elements:

1. App:- Type of Applications
2. Translated_Review:- Reviews being given by consumer
3. Sentiment:- Sentiment of trust from customer
4. Sentiment_Polarity:- It determines sentimental expression of the customer's opinion
5. Sentiment_Subjectivity:- Sentimental Subjectivity in terms is a personal opinion and it falls in range [0,1].

## Problem Questions:
1. Top Categories in Playstore?
2. Top Genres in the Playstore?
3. Top Content Rating per installation?
4. What is the percentage of free and paid Apps in the Play Store?
5. What is the effect of the last update on rating?
6. How does the last update have an effect on the trend of rating?
7. Effect on rating when the application was of type free and paid?
8. Relationship between reviews and rating?
9. relationship between Rating and Average Reviews
10. Average Rating of each App category
11. Average Rating for each genre
12. What is the distribution of sentiment subjectivity?
13. How sentiment polarity varies with Free and Paid Apps?
14. Different percentages of review sentiments based on two Datasets provided?
15. Different percentages of sentiment analysis on top 5 Reviewed App Categories?
16. Sentiment Analysis on each App Category
17. Sentiment Analysis on the basis of Genres
 
 
## Introduction:
Android as we know is a huge marketplace where every app developer has the opportunity. When Google acquired Android in 2005. Google incorporated the market with android in 2007 which have let developers develop android applications and in this way with very less association with their own developer and more on  open source developers it opened the markets of opportunities for both the makers and the user as well what we can easily speculate today. This has also helped in the development of many new businesses and also several new professions which we can experience now. 
There are basically three kinds of Applications in the Android Play Store. ‘Background Services and Intent Receivers Applications’,’Foreground Background Applications’ and ‘Intermittent Applications’.

The type of Applications which we will use to analyze in Play Store App Review Analysis mostly will be Intermittent type Applications.

In this project of Play Store App Review Analysis we will be analyzing each and every prospect of the data available with us and on the basis of this data we will try to solve every problem associated with the real world problem which lets them achieve customer prosperity.

## The following are the various steps involved in the EDA process:

1. Problem Statement - We shall brainstorm and understand the given data set. We shall study the attributes present in it and try to do a philosophical analysis about their meaning and importance for this problem.
2. Hypothesis - Upon studying the attributes present in the data base, we shall develop some basic hypothesis on which we can work and play with the data to look for the varied results which we can get out of it.
3. Univariate Analysis - It is the simplest form of analyzing the data. In this we would initially pick up a single attribute and study it in and out. It doesn't deal with any sort of co-relation and it's major purpose is to describe. It takes data, summarizes that data and finds patterns in the data.
4. Bivariate Analysis - This analysis is related to cause and the relationship between the two attributes. We will try to understand the dependency of attributes on each other.
5. Multivariate Analysis - This is done when more than two variables have to be analyzed simultaneously.
6. Data Cleaning - We shall clean the dataset and handle the missing data, outliers and categorical variables.
7. Testing Hypothesis - We shall check if our data meets the assumptions required by most of the multivariate techniques.

## DATA EXPLORATION, CLEANING AND INSIGHTS

1. App - It tells us about the name of the application.
2. Category - It tells us about the category to which an application belongs.
3. Rating - It tells us about the ratings given by the users for a specific application.
4. Reviews - It tells us about the total number of users who have given a review for the application.
5. Size - It tells us about the size being occupied the application on the mobile phone.
6. Installs - It tells us about the total number of installs/downloads for an application.
7. Type - It tells us whether the application is free or a paid one.
8. Price - It tells us about the price of the application.
9. Content_Rating - It tells us about the target audience for the application.
10. Genres - It tells us about the various other categories to which an application can belong.
11. Last_Updated - It tells us about the when the application was updated.
12. Current_Ver - It tells us about the current version of the application.
13. Android_Ver - It tells us about the android version which can support the application on its platform.

## Data Cleaning - Univariate & Bivariate Analysis

The number of null values in User-review dataframe are:

* Translated_Review has 26868 null values which contributes 41.79% of the data.
* Sentiment has 26863 null values which contributes 41.78% of the data.
* Sentiment_Polarity has 26863 null values which contributes 41.78% of the data.
* Sentiment_Subjectivity has 26863 null values which contributes 41.78% of the data.
Note1: 49% of NaN found in 4 features of user-review dataset hence we have removed all the NaN values from the user_review data frame.

The number of null values in play_store dataframe are:

* Rating has 1474 null values which contributes 13.60% of the data.
* Type has 1 null value which contributes 0.01% of the data.
* Content_Rating has 1 null value which contributes 0.01% of the data.
* Current_Ver has 8 null values which contributes 0.07% of the data.
* Android_Ver has 3 null values which contributes 0.03% of the data.

## Our Hypotthesis

1. Hypothesis_1:

We cannot simply drop these NaN values of Rating Column. So in order to get sentiment or translated review info for the apps from the user_review DF so that we can fill these NaN values based a logic based derivation. Thus, we need to merge these two DF's so that we get Common Apps between between them and can compare.

2. Hypothesis_1 conclusion:

We don't have infomation of sentiment of the Apps to fill the NaN values for the remaining apps from the merged DF.

3. Hypothesis_2:

Let us check whether do we have rating of Apps within the PlayStore DF.

4. Hypothesis_2 conclusion:

we found that even with this hypothesis we dont get information needed to fill NaN of the Rating.

Note2: Since both Hypothesis did not get us the information about Filling NaN values of Rating. We shall proceed with dropping these from the play_store DF.

## Conclusion:

So here we come at the end of our project which is play store App Review Analysis.What we have done just take a short recap. First we have done the removal of null value from rows and columns and the same goes with the removal of duplicates from the datasets. Then we did the formatting for each of the required columns in each dataset. 
After analyzing the data we conclude that App with the category Family and the genre tools are in large numbers. Also we can conclude that the number App Rating is directly proportional with the recent update. From this we can see that with all the major updates apps will get more ratings.
We can also conclude that most of the apps which are used by the users have a content rating of ‘Everyone’.
In percentage of Free and Paid App Available in the PlayStore we can assume that most apps being used by the users are Free. This shows very few users purchase Apps on playstore.
In rating vs count of App Type we conclude that rating is not get affected even if the app is paid or not but if we go on for finding the average rating we will find that free app will have less average rating compared to paid because of significantly high counts of free Apps as compared to Paid App available in App Store.
 
After moving forward when we performed analysis on sentiment subjectivity we found that most of the opinion on sentiment subjectivity lies high in the range 0.4 to 0.7.
When we analyzed sentiment polarity for paid and free Apps we noticed that sentiment polarity for free apps is way less than paid Apps.
In pie presenting the percentages of review sentiment we found that most of the sentiment are positive and neutral review is the lowest. Also in case finding the percentage of sentiments for  top 5 Apps we found among top 5 App Category Health and Fitness has received the highest positive sentiments while Game app category has received the highest negative sentiments and Sports App Category has received the highest neutral sentiments.
Important Points to be noted:
After merging both of the dataset we find an Average Rating of 4.32.
Also we can see that after merging both of the dataset the maximum Average Rating is 4.9.
Also the average sentiment Polarity is 0.16 and average sentiment_subjectivity is 0.49
Also we have noticed that the average size of the Application available on playstore is 21933.38 KB.
Lastly, all of the calculations and graphs  in this project have accuracy in the range of 75% to 80%.

Some other Insights:

• In this project of analyzing play store applications, we have worked on several parameters which would help AlmaBetter to do well in launching their apps on the play store. 
• In the initial phase, we focused more on the problem statements and data cleaning, in order to ensure that we give them the best results out of our analysis.  
• Developing apps related to the least categories as they are not explored much. Like events and beauty. 
• Most of the apps are Free, so focusing on free app is more important. 
• Focusing more on content available for Everyone will increase the chances of getting the highest installs. 
• They need to focus on updating their apps regularly, so that it will attract more users. 
• They need to keep in mind that the sentiments of the user keep varying as they keep using the app, so they should focus more on users needs and features.

## References
1. GeekforGeeks
2. Kaggle
3. Analytics Vidya


