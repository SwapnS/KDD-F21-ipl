# KDD-F21-ipl

## Team Members:
1) Swapn Shah
2) Snigdha Bhagat 
3) Mohammed Sharik U Zama

## Introduction:

Cricket is also referred as Game of Uncertainty and there is no precise forecast that can predict a specific team would win in any given conditions. Popularity of cricket increased when ICC (International Cricket Council) started concept of fast cricket in the form of twenty-20(T-20) matches. 

IPL is a franchise-based T-20 Cricket competition organized by BCCI (Board of Control for Cricket in India). The first season of IPL was played in 2008 and its popularity is increasing ever since. Within a short period, IPL has become the highest revenue generating league of India.

Data Analytics has been a part of Sports entertainment for a long time and being a cricket fan visualizing the statistics of cricket is mesmerizing. With the help of past data and knowledge base, we aim to use the Existing Data Analysis and Machine learning techniques to predict the winner of a particular IPL match after one inning.



## Data Sources and Domain Knowledge : 

1) https://www.kaggle.com/patrickb1912/ipl-complete-dataset-20082020
2) https://stats.espncricinfo.com/ci/engine/records/index.html?id=117;type=trophy
3) https://arxiv.org/pdf/1809.09813.pdf

Results of every match in the IPL depends on the various conditions like venue, player performance, toss, performance in power play etc.

By using all the necessary information, we are planning to build a classifier which predicts the winner or the winning probabilities for the playing teams
after the first innings.

Also, a regression task can be implemented which can predict runs scored by current batting team at the end of the inning.

## Exploratory Data Analysis:

Exploratory Data Analysis is done on the datasets. 

Firstly, several irrelavant features like 'eliminator', 'method', 'umpire1', 'umpire2', 'result_margin' and etc were removed from the datasets

A dictionary with key value pair of the team's name and it's appropriate abbreviation is created. So that we can get rid of the long team names

Next, missing value analysis and handling is done on the datasets. This involved imputing the null values in city based on venue.

Then, the visualization of teams with most wins in IPL seasons and the team with most toss wins was done. This led on to a discovery that toss is an important factor in a IPL match. Then further exploration of data was done by looking at how the teams performed when they were batting first and bowling first.

- Most wins by any ipl team over the years. 

![Most_wins_IPL](https://user-images.githubusercontent.com/91851356/145313277-0aa5f3b4-3102-4f25-a0d5-b1374ac2d964.png)

- Most Toss wins by an ipl team 

![number of tosses won](https://user-images.githubusercontent.com/91851356/145313445-0c985563-83d3-4dc0-b7a5-ea193de91385.png)


Here you can observe how toss is a very important factor in a cricket match.

- Batting First Winning percentage 
![Batting_First_win](https://user-images.githubusercontent.com/91851356/145313485-dbc2f50b-65ba-4f57-b6e3-a32d97746467.png)


- Bowling First Winning percentage



Here, It is evident that how some teams are good at defending a total and some teams are good at chasing a total. 


After that, data is prepared for modeling. Here, we removed 'toss_winner' and 'winner' as we have created 2 different variables similar to them previously. And we furthur encoded the remaining variables of the dataset.
![Bowling_First_win (1)](https://user-images.githubusercontent.com/91851356/145326641-cc1d6ea9-727a-4221-8116-fab1b888f33c.png)



## Data Preparing 

Initially, Our dataset did not had enough features for a predictive task. The average accuracy of the classifiers is around 0.50-0.55. 
- To overcome this issue, we inroduced new features to our dataset.
- Also we performed feature encoding to certain variables as well.

In an ipl match you can most accurately determine the outcome after the first innings. Since a lot of factors depend upon the outcome. For example,
if a team scores high runs by batting first, the chasing team will be in immense pressure while chasing the target so that's why we included a variable
named "total_runs". Also, we added another feature named "is_wickets" so that we can get an idea about the wickets lost by team which is batting first. 

-Another important factor is the venue where teams are playing. For example, if a team is playing in home condition then it will be beneficial. 
To consider this issue, we introduced another variable named "team1_home" which is 1 if the team1 is playing at home ground otherwise 0.
Also, some of the ipl matches are played outside of india meaning at neutral venue. for that, we introduced a variable named "neutal_venue". 
These two variables can determine that which team has home advantage.

## Machine Learning

To predict the outcome we trained 5 different models.
1.) Naive bayes
2.) Decision Trees
3.) Random Forest 
4.) XGBoost Classifier
5.) ADABoost Classifier

We also used "DataBricks" Platform to develop machine learning models online on our dataset. 

We used RandomizedSearch CV for hyperparameter tuning as GridsearchCV takes long time to train the model.


## Evaluation

For the Evaluation purpose, we used training scores, test scores and cross validation scores of our models. 

Out of all, RandomForest model achieved the highest score among all the classifiers. 


- Training Accuracy 

 * Gaussian NB :  0.600924499229584
 * Decision Tree :  0.7688751926040062
 * Random Forest :  0.8382126348228043
 * XGBoost  :  0.7411402157164869
 * ADABoost  :  0.5731895223420647


-Test Accuracy 

* Gaussian NB :  0.5337423312883436
* Decision Tree :  0.5828220858895705
* Random Forest :  0.7116564417177914
* XGBoost  :  0.6809815950920245
* ADABoost  :  0.558282208588957


- Cross Validation Score

![IPL_Model_Evaluation (2)](https://user-images.githubusercontent.com/91851356/145317992-1e39340a-9585-42e3-8f3e-3a9cdc7690e2.png)

-  Databricks Model Performance
<img width="1200" alt="Screen Shot 2021-12-08 at 17 16 08" src="https://user-images.githubusercontent.com/91851356/145318435-c1deb2d6-9aa8-46b9-b264-b726923657a5.png">


- Feature Impact 
<img width="1114" alt="Screen Shot 2021-12-08 at 16 54 17" src="https://user-images.githubusercontent.com/91851356/145318460-8a72119f-9633-48bf-94b7-aadb51c3bf18.png">


## Conclusion

We have 2 datsets with us. one with every ball delivered and another with the outcome of every match. One of the major challenge we faced to get the best 
of them. We had to create multiple features in order to improve the performance of the models. We used accuracy as evaluation metrics. One of the most difficult challenge we faced was to improve the performance of our models and create new features for our dataset.

## Future Scope
In the future, we would like to implement LSTM networks and also we can try to add the date feature to include time-series evaluation to see whether 
it impacts the performance or not. 



