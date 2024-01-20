---
title: "Steam Game Recommendation Analysis"
collection: publications
permalink: /publication/2009-10-01-paper-title-number-1
excerpt: 'A project related to big data, python, and SQL.'

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
includes information on ratings, pricing in US dollars, release dates, among other details. 
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
Structured or Unstructured: This is structured data, as it is organized in a tabular format with 
rows and columns.  
**Source and Collection Details:** The dataset was collected from Steam Official Store. All rights 
on the dataset thumbnail image belong to the Valve Corporation. The expected update 
frequency is Monthly.  

