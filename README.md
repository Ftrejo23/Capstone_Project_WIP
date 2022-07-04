# Capstone_Project - WORK IN PROGRESS

## Data Dictionary
|Feature|Type|Description|
|---|---|---|
| console | object |electronic device that outputs a video signal or image to display a video game|
| video_game_name |object | name of video game|
| summary |object | summary of what video game is about|
| developer |object | the developer (creator) of the video game|
| genre(s) |object | genre of video game|
| num_players* | int| max number of players that can play in the same game environment at the same time|
| esrb_rating |object | ESRB (Entertainment Software Rating Board) rating of video game|
| critic_score |int| critic review score of video game|
| avg_user_score |float| average user review score of video game|
| user_review |object | user review of video game|
| user_score |int|user score of video game |

\* values of 100 - games with online multiplayer <br>
\* values of 150 - games considered to be MMOs (massive multipler online games)

## PROGRESS REPORT
**Student Check-in:**

### Part 2
|WHAT’S GOING WELL/STRUGGLES|DEVELOPMENT PLAN|INSTRUCTOR FEEDBACK|
|---------------------------|----------------|-------------------|
|-scraping web pages went well despite a lot of trial and error with the web scraper|   |      |
|-preliminary data cleaning also went well|                |                   |
|- no huge struggles yet, spent a lot of time troubleshooting for web scraper and data cleaning but was eventually able to get desired results  |                |                   |
|-there is a lot of reviews, wondering if I should random sample a smaller subset? When I get to modeling run time could be pretty long |                |                   |

### Part 3
|WHAT’S GOING WELL/STRUGGLES|DEVELOPMENT PLAN|INSTRUCTOR FEEDBACK|
|---------------------------|----------------|-------------------|
|We have 9 columns that we can do EDA on which includes are target variable. Created functions to help with EDA.|   |      |
|For continous variables, looked at scatter plot with target and plotted frequency of the variable.|   |      |
|For categorical variables, looked at value counts and grouped by variable to see relationship with target|   |      |
|We identified a few outliers in our data, specifically in our target variable that we may want to remove prior to modeling.|   |      |
|We also found that we have class imbalance in some of our features. Feature engineering may be our best approach to circumventing this issue.|   |      |
|The way we currently have our target set up (above/below median average user score) creates an imbalance in how many unique games in our data set fall above/below our target. Roughly only 127 out of 425 video games are above the median BUT that still equates to 50% of our dataset since we have individual reviews per game. Maybe just talking this through can help identify whether this even is an issue or not.  |   |      |