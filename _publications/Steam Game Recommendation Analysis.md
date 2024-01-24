---
title: "Steam Game Recommendation Analysis"
collection: publications
permalink: /projets/Steam Game Recommendation Analysis
excerpt: 'A project related to big data, python, and SQL.'
date: 2023-12-07
---



This project provides a comprehensive analysis of player experiences on the Steam 
gaming platform, focusing on game reviews and user engagement. Through 
quantitative textual analysis, it identifies patterns in player feedback, highlighting the 
most popular and critically acclaimed games. The project also introduces a recommender 
system developed using Python, offering personalized game suggestions based on user 
preferences and review content. Insights from this project are pivotal for game 
developers and industry stakeholders, underlining the importance of user reviews in 
game development and marketing strategies. The project concludes with 
recommendations for enhancing user experience on Steam.
<br>
<br>

**Project Motivations**
-----------------
The comprehension of player experience frequently presents challenges, and it is not 
always evident to game developers which aspects of a game should be retained or discarded 
(Busurkina et al.,2020). From the player's perspective, in order to enhance their understanding 
of games and provide personalized game recommendations, the analysis of specific game 
reviews becomes instrumental. This approach can facilitate the development of superior quality 
games, while concurrently gaining insights into player psychology and gaming inclinations. 

The primary objective of our exploratory project was to discern the criteria by which individuals 
assess their gaming experiences, specifically through reviews posted on the Steam platform.
In our project, we try to understand the important features of game experience using 
quantitative textual analysis of game reviews on the Steam platform.
This project enhances the comprehension of mechanisms for consumer retention, 
corroborating the notion that reviews are instrumental in product improvement. Efficient 
utilization of reviews can boost sales, given that electronic word-of-mouth exerts a more 
favorable impact on purchasing decisions compared to traditional face-to-face word-of-mouth 
(Mankad et al., 2016).
<br>

**Description of the Data**
-----------------
The dataset for the "Steam Game Recommendation Analysis" project is sourced from Kaggle and comprises three primary CSV files: games.csv, users.csv, and recommendations.csv, each contributing uniquely to the analysis of video game trends and preferences.

**1. games.csv**  

This file contains tabular data regarding various games or add-ons, which 
includes information on ratings, pricing in US dollars, and release dates, among other details. 
Additional non-tabular metadata about the games, such as descriptions and tags, are contained 
in a separate metadata file.  
**Number of Records:** The dataset contains 50,872 records.  
**Number of Features:** There are 13 features (columns) in the dataset.  
**First Few Rows:** A glimpse into the dataset reveals columns like 'app_id', 'title', 'date_release', 
platform compatibility (Windows, Mac, Linux), 'rating', 'positive_ratio', 'user_reviews', pricing 
details, 'discount', and 'steam_deck' compatibility.  
**Data Types:** The data types include integers (int64), floating-point numbers (float64), boolean 
(bool), and objects (object). The 'date_release' column is currently in an object (string) format, 
which might need conversion to a DateTime format for certain types of analysis.  
**Structured or Unstructured:** This is structured data, as it is organized in a tabular format with 
rows and columns.  
**Source and Collection Details:** The dataset was collected from the Steam Official Store. All rights 
on the dataset thumbnail image belong to the Valve Corporation. The expected update 
frequency is Monthly.  

**2. users.csv**  

This file encompasses tabular data on Steam's registered user profiles, detailing their engagement and purchasing behavior through the platform.  
**Number of Records:**  According to the description, the dataset is extensive, containing 13,786,778 records, reflecting a vast user base.  
**Number of Features:** The file includes 3 distinct features, providing a focused insight into user activity.  
**First Few Rows:** The initial data rows would typically display individual user IDs alongside their product purchase count and review count.  
**Data Types:** ALL the specific data types are integers (int64).   
**Structured or Unstructured:**  This dataset is structured, presenting information in a clear, tabular format conducive to analysis.   
**Source and Collection Details:**  The data is sourced from the Steam platform, indicating a comprehensive aggregation of user interaction data, which may be updated periodically.   

**3. recommendations.csv**  

This file consists of data regarding user-generated reviews and recommendations for games on the Steam platform, offering a multifaceted view of user engagement.  
**Number of Features:**  The dataset includes several features such as 'app_id', 'helpful', 'funny', 'date', 'is_recommended', 'hours', 'user_id', and 'review_id'.  
**First Few Rows:** The initial rows likely present individual reviews, including user engagement metrics and the recommendation status. 
**Data Types:**  Data types in this file include integers, booleans, and datetime objects, indicating a mix of quantitative and categorical data.   
**Structured or Unstructured:** Given the tabular format with distinct rows and columns, the dataset is structured.  
**Source and Collection Details:** The data has been collated from user interactions on the Steam platform, with the potential for monthly updates to reflect ongoing user activity.

**Problem Statement**
-----------------
1. Which game has the most reviews in total?
2. Which game has the most helpful/funny reviews?
3. Which game is the most recommended by users?
4. What are the Top 10 rated Steam games released?
5. What are the Lowest 10-rated Steam games released?
6. What is the distribution of Game ratings?
7. Recommendations to users based on game similarities

**Research Method**
-----------------
To solve problems 1-6, we use Impala to query and analyze data using SQL-like syntax and then use Python and Tableau to visualize the results.
To solve problem 7, we use Python, specifically leveraging the pandas, matplotlib, pyspark, and scikit-learn libraries.

