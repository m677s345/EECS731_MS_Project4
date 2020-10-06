# EECS731_MS_Project4
  NFL, MLB, NBA and Soccer scores
1. Set up a data science project structure in a new git repository in your GitHub account
2. Pick one of the game data sets depending your sports preference
https://github.com/fivethirtyeight/nfl-elo-game
https://github.com/fivethirtyeight/data/tree/master/mlb-elo
https://github.com/fivethirtyeight/data/tree/master/nba-carmelo
https://github.com/fivethirtyeight/data/tree/master/soccer-spi
3. Load the data set into panda data frames
4. Formulate one or two ideas on how feature engineering would help the data set to establish additional value using exploratory data analysis
5. Build one or more regression models to determine the scores for each team using the other columns as features
6. Document your process and results
7. Commit your notebook, source code, visualizations and other supporting files to the git repository in GitHub

The goal of this project is to explore different Regression tools. From these regression tools we are tasked with determining the scores of the games from a sport we selected. I choose to do major league baseball. I thought that this is a sport that has a history of data collection and the records will be fairly complete and there are a lot of different statistics to model and potentially use as features. 
After exploring the data I found that the dataset I was using had only a handful of statistics that can be used in determining the final score of the game. I used ELO and the rating based on the ELO as the main features to determine the runs per game. I did not know how the ELO factored the runs into the value so I took the difference between the ELO and ratings from before the game was played and after as a feature. If the team lost the game their ELO decreased giving a negative number.
I cubed the difference of the statistics to retain the sign of the value. This gave me a much higher accuracy (max of 50%) for prediciting the final score of the game. I am sure that there are different perhaps specific models for regressing baseball statistics from ELO but overall this attempt can be improved by the addition of statistics directly related to the runs scored.
