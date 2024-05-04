# Capstone-Project-IPL-Match-Win-Prediction

![image](https://github.com/Ankit-770/IPL-Win-Prediction-project/assets/90442965/1699d619-276b-4f88-83c5-f2d0669a9a96)


Forecasting the likelihood of a team's victory in the Indian Premier League (IPL) is a critical business challenge for franchises, bookmakers, advertisers, and sponsors. Achieving the optimal prediction is of vital importance as it directly impacts various stakeholders.

Franchises: Provisioning the right team composition and strategic decisions to maximize win probability while managing costs.
Bookmakers: Ensuring precise odds and managing risks associated with betting outcomes.
Advertisers and Sponsors: Investing in teams with higher win probabilities to maximize their ROI and brand exposure.

Accurate win prediction models can help IPL teams enhance team performance, optimize resource allocation, and improve fan engagement. Moreover, it assists betting entities in facilitating informed betting decisions, which drives higher engagement, and helps advertisers and sponsors make data-driven investment choices for promoting their brands.
Therefore, developing a robust win prediction mechanism is essential to capitalize on opportunities, minimize risks, and ensure the overall success and sustainability of IPL franchises and associated stakeholders.

## Problem Statement

As the Indian Premier League (IPL) continues to grow in popularity, the accurate prediction of match outcomes has become increasingly essential for multiple stakeholders, including franchises, bookmakers, and advertisers. The main challenge lies in developing a reliable model to predict the probability of a team's victory in each IPL match. The goal is to create a robust prediction mechanism that accurately forecasts the likelihood of a specific team winning an IPL match. This crucial prediction not only impacts team strategies, but also serves as the basis for betting decisions, sponsorship investments, and marketing strategies. Therefore, the core aim of this project is to develop a reliable win prediction model that can provide invaluable insights for IPL franchises, betting entities, advertisers, and ultimately enhance fan engagement through informed and accurate predictions of match outcomes.

## Data Overview

This data was gathered during (2008-2019) IPL Matches. Data description is as follows;

Match Dataset:

1. id - Unique match ID
2. Season - match belong to which season
3. city - match host city
4. date - date of the match
5. team1, team2 - teams competing against each other
6. toss_winner - which team won the toss
7. toss_decision - decision of the team to bat or ball first
8. result - type of match result
9. dl_applied - is dl applied in the match
10. winner - which team won the match
11. win_by_runs - match win by runs
12. win_by_wickets - match win by wickets
13. player_of_match - best player of the match
14. venue - host stadium information
15. umpire1,2,3 - umpire information

Delivery Dataset:

1. match_id - match id of the match
2. total_runs_x - 1 team runs
3. inning - 1 or 2 inning information
4. batting_team - batting team information
5. bowling_team - bowling team information
6. over - over information
7. ball - ball of the over information
8. batsman - batsman info.
9. non_striker - non_striker batsman info.
10. bowler - bowler info.
11. is_super_over - super over info.
12. wide, bye, legbye, noball, penalty, batsman, extra, total runs - runs information of batting team
13. player_dismissed - player out info.
14. dismissal_kind - mathod of player dismissed
15. fielder - fielder information

## Approach
The following steps were followed in the project:

Data Preprocessing: The dataset was preprocessed and cleaned to handle missing values, outliers, and any inconsistencies in the data.

Data Split: The preprocessed data was split into training and test sets on a random state of 1. By using training data we trained our predictive model and we used testing data to evaluate our prediction.

Model Training:The models were trained using the training data, and their performances were evaluated using various metrics.

Model Evaluation: The performance of the trained models was evaluated using Accuracy & Cross- Validation. The model that performed the best on the test data was selected.

Model Deployment: The selected model can deployed using pickle, where it could make real-time predictions of ipl match result. The model's performance can monitor over time to ensure its accuracy and usefulness.

## Models Used
For modeling we tried various regression models such as- 
1)Logistic Regression

2)RandomForest

3)DecisionTree

4)KNeighbors

5)Gradient Boosting

## Results
From the score we can see that Gradient boosting classifier model is best model for our data it show most balanced result without over fitting values. Here we get optimal number of score which is 83.57% accuracy, which is best without over fitting the model. And this problem can be solved using this model.

## Outputs

Gradient Boosting
![image](https://github.com/Ankit-770/IPL-Win-Prediction-project/assets/90442965/16542ca5-ef2a-40b6-a19c-6b32d4ba633a)

Logistic Regression
![image](https://github.com/Ankit-770/IPL-Win-Prediction-project/assets/90442965/068cdbcd-8715-4c87-8e87-523997b2a55f)



## Conclusion
During our analysis, Firstly I cleaned the data and conducted an exploratory data analysis (EDA) on all the features in our dataset. Firstly, I analysed my dependent variable 'Win probability' and applied transformations as per requirement.Then I analysed Independent Variables both numerical and categorical variables. I have done Monovariate and Bivariate analysis on these variables . I also studied the numerical variables, calculated their correlations, and the their relationships with the dependent variable. I also applied Scaling to numerical varibale .

I employed 5 machine learning algorithms including Logistic Regression, DecisionTree, KNeighbors, Random Forest and Gradient Boosting . I also performed Feature scaling to enhance the performance of our models.

Some facts based on analysis:

1)The analysis revealed Important decision about the match, most consistent batsman and bowler information, most popular city and stadium for match, and various important aspects of the match are revealed in EDA.

2)To predict probability of the match, i have selected 11 key attributes: batting_team, bowling_team, city, current_score, runs_left, balls_left, wickets, total_runs_x, crr, rrr and result (these ate categorical and numerical columns). These attributes were divided into 80% of training and 20% testing data, and one hot encoding is apply on categorical data and standard scaler apply on numeric data.

3)In RandomForest Classifier model show 99.87% accuracy, which is highest in all models. but it may show over fitting in the results so I choose 'Gradient Boosting Classifier' and 'Logistic Regression' as best model with balanced accuracy score

4)we got to know that 'mumbai indians' & 'chennai super kings' is most consistent team who win maximum amount of matches.

5)for most of the teams chance of wining the match is high when they won the toss.
