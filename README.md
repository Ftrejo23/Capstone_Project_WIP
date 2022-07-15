# Video Game Average User Score Classification Project - WIP

## Contents

- [Problem Statement](#Problem-Statement)
- [Project Directory](#Project-Directory)
- [Data Dictionary](#Data-Dictionary)
- [Executive Summary](#Executive-Summary)
- [Conclusions & Recommendations](#Conclusions-&-Recommendations)

## Problem Statement

Video games take years of development time and cost anywhere from a few million to well over a hundred million dollars to produce. There are plenty of examples of video games that are poorly received and never establish a lasting player base. There are a few potential metrics that may determine how a game performs. One metric that can determine how a game performs is video game reviews, particularly what users score a game. Using video game reviews from Metacritic we want to create a model that will help us identify the attributes of a video game that will help it get a high average user score.

## Project Directory
```
Capstone_Project
|__ code
|   |__ 01_Web_Scraping_Metactritic.ipynb
|   |__ 02_Data_Cleaning.ipynb
|   |__ 03_EDA_&_Preliminary_Analysis.ipynb
|   |__ 04_Preprocessing.ipynb
|   |__ 05_Modeling.ipynb
|__ data
|   |__ cleaned_all_console_reviews.csv
|   |__ df_for_further_nlp.csv
|   |__ final_all_console_reviews.csv
|   |__ final_reviews_modeling.csv
|   |__ top_100_pc_games.csv
|   |__ top_100_ps4_games.csv
|   |__ top_100_ps5_games.csv
|   |__ top_100_switch_games.csv
|   |__ top_100_xbox-series-x_games.csv
|   |__ top_100_xboxone_games.csv
|__ README.md
```

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

## Executive Summary
For this project, we set out to get various user reviews for the top 100 all-time games from [Metacritic](https://www.metacritic.com/browse/games/score/metascore/all/ps4/filtered) for 6 different consoles. Using the Requests library and BeautifulSoup we were able to scrape over 100k reviews. All of the reviews were combined into a master data frame to use in our model to help identify the attributes of a video game that will help it get a high average user score.

The next step was to clean our data. Null values were addressed, and values were imputed and cleaned. Using cleantext and the clean function all of the text values in our dataset were also cleaned. Numbers were tokenized and emojis were removed as part of the cleaning process. With a clean dataset, we were able to move on to exploratory data analysis.

During EDA every column was explored. The target column was calculated by checking if the review is for a game above/below the median average user score of 8.4. Continuous features were explored using a scatter plot and a box plot. Categorical features were explored using bar charts and grouped bar charts with the target. Once all features were explored it was time to proceed with preprocessing.

For preprocessing all categorical variables were dummied. For video game names and developers we feature engineered custom columns to deal with all the unique values, some of which had only a few occurrences. From there we vectorized our columns with text values and explored the words that had a TF-IDF score of 1. We then condensed our data into a final .csv file ready for modeling.

For modeling, we used a Logistic Regression and Random Forest model for their interpretability. A grid search was performed for both models to find the best hyperparameters. Coefficients were extracted and interpreted in relation to our target. A confusion matrix was also created along with a classification report to see what was the precision and recall. The random forests model produced the highest accuracy score but due to its lack of interpretability with its coefficients emphasis was made to improve the logistic regression model. Text features were lemmatized and vectorized and then re-run in our logistic regression model. Coefficients were once again extracted and examined, successfully identifying the top 10 features to improve the chances of a game having a score above the median average user score of 8.4.



## Conclusions & Recommendations
Conclusion here.
