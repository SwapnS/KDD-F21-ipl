# KDD-F21-ipl

## Team Members:
1) Swapn Shah
2) Snigdha Bhagat 
3) Mohammed Sharik U Zama

## Introduction:

Cricket is also referred as Game of Uncertainty and there is no precise forecast that can predict a specific team would win in any given conditions. Popularity of cricket increased when ICC (International Cricket Council) started concept of fast cricket in the form of twenty-20(T-20) matches. 

IPL is a franchise-based T-20 Cricket competition organized by BCCI (Board of Control for Cricket in India). The first season of IPL was played in 2008 and its popularity is increasing ever since. Within a short period, IPL has become the highest revenue generating league of India.

Data Analytics has been a part of Sports entertainment for a long time and being a cricket fan visualizing the statistics of cricket is mesmerizing. With the help of past data and knowledge base, we aim to use the Existing Data Analysis and Machine learning techniques to predict the winner of a particular IPL match.


## Target Population: 
Cricketers playing in various teams of Indian Premier League from 2008 to 2020.


## Research Questions:

What is the probability of winning a match given features like previous player performance, venue and 
other match related data is available?

What are the top features that affect the chances of winning the match?

Prescriptive analysis to see which batsman is good against which bowler and vice versa

We aim to develop some meaningful features such as prior probabilities of winning for each team, prior probability of team winning the cup etc. 

## Data Sources: 
1) https://www.kaggle.com/patrickb1912/ipl-complete-dataset-20082020
2) https://stats.espncricinfo.com/ci/engine/records/index.html?id=117;type=trophy

Results of every match in the IPL depends on the various conditions like venue, player performance, toss, performance in power play etc.

By using all the necessary information, we are planning to build a classifier which predicts the winning probabilities for the playing teams.

Also, a regression task can be implemented which can predict runs scored by current batting team at the end of the inning.

## Exploratory Data Analysis:

Exploratory Data Analysis is done on the datasets. 

Firstly, several irrelavant features like 'eliminator', 'method', 'umpire1', 'umpire2', 'result_margin' and etc were removed from the datasets

A dictionary with key value pair of the team's name and it's appropriate abbreviation is created. So that we can get rid of the long team names

Next, missing value analysis and handling is done on the datasets. This involved imputing the null values in city based on venue.

Then, the visualization of teams with most wins in IPL seasons and the team with most toss wins was done. This led on to a discovery that toss is an important factor in a IPL match. Then further exploration of data was done by looking at how the teams performed when they were batting first and bowling first.

After that, data is prepared for modeling. Here, we removed 'toss_winner' and 'winner' as we have created 2 different variables similar to them previously. And we furthur encoded the remaining variables of the dataset.

Finally, data modeling id done by using GaussianNB from sklearn library followed by computing the Accuracy Score 


