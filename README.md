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

|WHAT’S GOING WELL/STRUGGLES|DEVELOPMENT PLAN|INSTRUCTOR FEEDBACK|
|---------------------------|----------------|-------------------|
|-scraping web pages went well despite a lot of trial and error with the web scraper|   |      |
|-preliminary data cleaning also went well|                |                   |
|- no huge struggles yet, spent a lot of time troubleshooting for web scraper and data cleaning but was eventually able to get desired results  |                |                   |
|-there is a lot of reviews, wondering if I should random sample a smaller subset? When I get to modeling run time could be pretty long |                |                   |