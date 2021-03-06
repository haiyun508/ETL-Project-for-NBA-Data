# Project Report

## Extract

The sources we are using in this project is csv files from Kaggle (https://www.kaggle.com/open-source-sports/mens-professional-basketball?select=basketball_awards_players.csv) and data.world (https://data.world/datadavis/nba-salaries) with data about NBA players, NBA teams and NBA coaches from 1937 to 2012


## Transform

After reading each csv file to python and create a dataframe, we find out each csv file has much more information than we need, so we clean the data by dropping those unnecessary and duplicated information. For easy access and reference in later analysis, we rename the keys names.

When summarizing the coaches master, we decide to merge coaches awards dataframe with coaches dataframe to get all the information about the coaches including their award details before loading it to sql database. 

Finally, we have six dataframes with cleaned data:players_df; awards_df; salary_df; teams_master_df; coaches_master_df;team_summary_df.

## Load

With the information we have, we were able to creat two relational databases: basketball_db with three tables inside:players,awards and salaries and NBA_DB with three tables inside:teams_master,teams_summary and coaches_master.

We load the data previously cleaned up to the above database and confirm all the data is loaded successfully.

Some queries were done across the relational database basketball_db and we were able to get a complete dataframe with all the players' information we are interested including player_id, last_name, first_name, awards_count and max salary. 


# Analysis
Get a tableframe with data about top players with more than ten awards 

Get a tableframe with data about players with top ten max salaries

A regression analysis is conducted to show the relationship between players' awards_count and max salary.
It turned out there is no significant relation between players' awards_count and max salary. The reason could be players who played basketball for many years tend to have more awards and salary years ago can not match today's and young players with less awards tend to have high salary with current salary standard.

Team level data was analyzed. We analyzed the length of years each team have been in NBA games. According to the data highest number of years were played by New York Knicks and Chicago Bulls, which is 45 years. 

When analysing this data it is evident that some of the name changes of teams have an effect on the evaluation. To improve the accuracy of this evaluation team name changes should be incorporated in to the analysis.

Also the % of games won by each team was also analysed . 
