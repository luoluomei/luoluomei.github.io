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

**Results**
-----------------
**1. Which game has the most reviews in total?**

According to the chart provided, “Team Fortress 2” received the most reviews among the 
top 10 games. The bar chart shows that “Team Fortress 2” has garnered over 300,000 reviews, 
making it the most reviewed game on the list. The games that followed "Team Fortress 2" were 
"Rust," "Cyberpunk 2077," "Counter-Strike: Global Offensive," "Dota 2," "The Witcher 3: 
Wild Hunt," "Paladin," "Fallout 4," "Wallpaper Engine," and "Tom Clancy's Rainbow Six 
Siege," all with significant numbers of reviews.  

Team Fortress 2's high reviews reflect its long-term popularity and strong gaming 
community. It is worth noting that Team Fortress 2 has been on the market for quite some time, 
which has also contributed to the large number of reviews it has accumulated. In addition, the 
emergence of new games such as Cyberpunk 2077 shows that recently released games can also 
receive a large number of reviews, which may be due to the initial hype and the large player 
base at launch. Overall, the number of reviews a game receives can reflect its popularity, the 
size of its player base, and community activity.  
<br>
<br>
![Q1](/images/1.png)
<br>

**2. Which game has the most helpful/funny reviews?**

The following two charts show the top 10 games that received both "helpful" and "funny" 
votes. Interestingly, the top three are the same. Looking specifically at the first chart, "Counter-Strike: Global Offensive" leads in the 
number of votes helped, followed by "PUBG" and "Grand Theft Auto V." The remaining 
games, including "Cyberpunk 2077," "No Man's Sky," "DayZ," "Tom Clancy's Rainbow Six 
Siege," "Fallout 4," "Dota 2," and "The Witcher 3: Wild Hunt," had significantly fewer 
beneficial votes, indicating a strong preference for or reliance on the leading game for beneficial 
community feedback.  

In the second chart, "Counter-Strike: Global Offensive" also topped the funny vote, but 
by a much larger margin than "PUBG”, which came in second. The funny category vote was 
not as evenly distributed as the good category vote, with a sharp drop after the top two games. 
The list includes "Grand Theft Auto V," "Tom Clancy's Rainbow Six Siege," "Dota 2," "The 
Forest," "Wallpaper Engine," "Rust," "The Witcher 3: Wild Hunt," and "Cyberpunk 2077."  

Based on these observations, we can conclude that “Counter-Strike: Global Offensive” is 
not only viewed by the community as a rewarding game but also as a source of entertainment, 
coming out on top in both beneficial and fun polls. "PUBG " and "Grand Theft Auto V" also 
received high ratings in both categories. The number of votes for funny games after the top two 
dropped sharply, suggesting that humor may be more concentrated in certain gaming 
communities. Games like "The Forest" and "Wallpaper Engine" appear on the funny poll, but 
not on the helpful poll, which may indicate that these games are more popular for their 
entertainment value than for their informative community feedback.
<br>
<br>
![Q21](/images/21.png)
<br>
![Q22](/images/22.png)
<br>

**3. Which game is the most recommended by users?**

The pie chart below displays the distribution of user recommendations among the top 5 
games. "Team Fortress 2" is the most recommended game with 27.1% recommendations. 
"Rust" follows closely with 20.8% of recommendations, while "The Witcher 3: Wild Hunt", 
"Wallpaper Engine" and "Counter-Strike: Global Offensive" have 17.8%, 17.2% and 17.1% 
respectively.  

The high percentage of recommendations suggest that the game is highly favored within 
their communities, reflecting a strong level of satisfaction and positive endorsement from the 
users who have reviewed them.  
<br>
<br>
![Q3](/images/3.png)
<br>

**4. What are the Top 10 rated Steam games released?**

We selected games with a positive ratio above or equal to 90 and a rating of 
'Overwhelmingly Positive'. Then listed it in descending order of user reviews and positive ratio 
to get the Top 10 rated steam games released. This process guarantees the exclusion of games 
with low user reviews, as lower reviews tend to result in less reliable and potentially distorted 
positive ratios and ratings.  

Below is the result of the Top 10 rated steam games released. We can see that the top 1 
game is Terraria with 943413 user reviews and 97 positive ratios.
<br>
<br>
![Q4](/images/4.png)
<br>

**5. What are the Lowest 10-rated Steam games released?**

Similar to the previous question, we eliminate games with low user reviews, as lower 
reviews often lead to less dependable and potentially skewed positive ratios and ratings. We 
selected games with a positive ratio below or equal to 50 and a rating of either 'Overwhelmingly 
Negative', 'Mostly Negative' or 'Negative', the bottom three rating classifications. Then listed it 
in descending order of user reviews and in ascending order of positive ratio to get the lowest 
10 rated steam games released.  

We can see from the results below that the lowest game is Overwatch 2 with 181198 user 
reviews and 9 positive ratio.
<br>
<br>
![Q5](/images/5.png)
<br>

**6. What is the distribution of Game ratings?**

We counted the number of games in each level of rating and got the chart below. 
According to the bar chart, we can see that games are on average rated more positively with 
most games falling between mixed and very positive. It was uncommon to find games rated on 
either extreme with only 1110 games rated as “Overwhelmingly Positive” and only 14 games 
as “Overwhelmingly Negative”.  

This situation is due to the Steam rating system. The rating system splits games into three 
groups, 10-49 reviews, 59-499 reviews and 500+ reviews. To achieve a 'Very Positive' or 
'Overwhelmingly Positive' rating, a game must have over 50 or 500 reviews respectively and 
with a positive review ratio of 80% or higher. Conversely, a negative rating is assigned when 
the positive review ratio is 19% or less.  

While this rating system explains for the little number of games in either extreme rating, 
it doesn't explain why most Steam games are positive. So relying solely on game ratings for 
recommendations may not be comprehensive, as a majority of games tend to receive positive 
ratings. These ratings alone may not provide sufficient information about a game's suitability 
for players. Additional factors and considerations beyond ratings are needed to make more 
informed recommendations, ensuring that the recommended games align with the preferences 
of the players.
<br>
<br>
![Q6](/images/6.png)
<br>
