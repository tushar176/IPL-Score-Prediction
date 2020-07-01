# IPL-Score-Prediction
 This model predict the score (in range) of Indian Premier League(IPL) which is deployed on the Heroku platform using flask(micro web framework).
- The link for the web app is-->https://predicting-ipl-scores.herokuapp.com/
- The GitHub Repo Link for the Deployment of the project is-->https://github.com/tushar176/Ipl-Score-Prediction-Deployment

## Demo Of Web App
![Demo Of Web App](https://github.com/tushar176/Ipl-Score-Prediction-Deployment/blob/master/demo.gif)

## Dataset
The dataset 'ipl dataset.csv' consists of ball-to-ball informations of every match of IPL from Season 1 to 10 ie: (2008 to 2017).

Dataset consists following columns:
- mid: Unique match id.
- date: Date on which the match was played.
- venue: Stadium where match was played.
- bat_team: Batting team name.
- bowl_team: Bowling team name.
- batsman: Batsman who faced that particular ball.
- bowler: Bowler who bowled that particular ball.
- runs: Runs scored by team till that point of instance.
- wickets: Number of Wickets fallen of the team till that point of instance.
- overs: Number of Overs bowled till that point of instance.
- runs_last_5: Runs scored in previous 5 overs.
- wickets_last_5: Number of Wickets that fell in previous 5 overs.
- striker: max(runs scored by striker, runs scored by non-striker).
- non-striker: min(runs scored by striker, runs scored by non-striker).
- total: Total runs scored by batting team at the end of first innings.

## Features Used for Prediction and Asumptions

  - **runs**(runs at a particular movement can be a very helpful in predicting the final score )
  - **wickets**( number of wickets fallen at a instance can also be very crutial for prediction as if less number of wickets fallen have a high chance of high score normally)
  - **overs**(over is also very important feature in prediction as at the start of the matchs player tends to score less runs as compared to the last 5 overs)
  - **striker**(player on the field have high score means its a good player,also is playing is the match for long and can hit a good score)
  - **non-striker**(it can also be helpfull in prediction ,like a low number of non stricker can lead to low runs and viceversa.)  

## Algorithms
- Linear Regession
- Rigde Regession
- Lasso Regession
- Decision Tree Regression
- Random Forest Regression

**Random Forest Regression gives the best score of 0.946(Get by using gridsearchcv on the parameter n_estimators =110) .So we have used Random Forest Regression for building model.**


## Future Scope
- Implementation using Artificial Neural Network (ANN).
- Adding more features(columns) like name of bowler, name of batsman etc.
