**By: Nathen Lee & Siddharth Vyasabattu**
# Introduction
Our project will build a classification model predicting the results, i.e, wins and losses, of  League of Legends professional teams in 2022 . Our model takes into consideration the various features provided as columns in the dataset. The dataset being used is a cleaned version of the data provided by https://oracleselixir.com/tools/downloads with rows and columns corresponding to our research focus. This dataset has 4948 total rows and 12 total columns. Each row in our dataset corresponds to a team’s statistics in a certain game.
The columns correspond to those statistics:
- <mark>gametype</mark> states whether the game was played on a regional stage or international stage. 
- <mark>league</mark> corresponds to the league/tournament the game was from.
- <mark>result</mark> declares whether or not a team won(1) or a team lost(0).
- <mark>kills</mark> corresponds to the total sum of the kills of each player of the team. 
- <mark>dragons</mark> corresponds to the total number of dragons the team killed over the course of the game.
- <mark>elders</mark> corresponds to the total number of elder dragons the team killed over the course of the game.
- <mark>heralds</mark> corresponds to the total number of rift heralds the team killed over the course of the game.
- <mark>barons</mark> corresponds to the total number of baron nashors the team killed over the course of the game.
- <mark>towers</mark> corresponds to the total number of towers the team destroyed over the course of the game.
- <mark>visionscore</mark> corresponds to the total sum of the vision granted or denied by the players on the team. 
- <mark>creepscore</mark> corresponds to the total sum of the minions and monsters killed by the players on the team.

# Framing the Problem 
We decided to work on the prediction problem of determining whether a team will win or lose a game. To achieve this, we are constructing a binary classifier model that utilizes the provided features to predict the outcome - whether the team won (1) or lost (0) a game. The information we'll be needing as features are: 'gametype', 'league', 'kills', 'dragons', 'elders', 'heralds', 'barons', 'towers', 'visionscore', and 'creepscore'. Given the unbalanced distributions of international and regional games, we evaluated the model's performance using the f1-score metric, as it is well-suited for classification problems of this nature.

# Baseline Model
Our baseline model utilizes a preprocessor to one-hot encode the gametype and league features and keeps the remaining features the same as they are passed through a decision tree classifier. Before preprocessing, the gametype and league features were both nominal features, but after preprocessing, all of the features used in our baseline model were quantitative. This model yielded an accuracy of 1.0 for our training set and ~0.95454 for our test set. Because of this, we determined that this model is not 'good' as the model is overfitting on the training set. To remove the overfitting issue, we must improve the model by altering more features and establishing an adequate depth for the decision tree.


# Final Model


# Fairness Analysis
<iframe src="assets/f1-score.html" width=800 height=600 frameBorder=0></iframe>
