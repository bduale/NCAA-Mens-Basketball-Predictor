# NCAA-Mens-Basketball-Predictor
Explore Kaggle's 2019 NCAA Mens Basketball dataset and create a predictor to predict future tournament winners

# Before Starting
Getting to Know About NCAA March Madness Tournament --> https://en.wikipedia.org/wiki/NCAA_Division_I_Men%27s_Basketball_Tournament

# Getting Dataset:
1. pip install kaggle
2. Sign up for Kaggle account (https://www.kaggle.com) 
3. Verify phone number for account
4. Go to My Account
5. Click Create New API Token (will download a kaggle.json file)
6. Place the kaggle.json file in the .kaggle folder created by installing kaggle (C:/users/username/.kaggle)
7. Accept the rules of the competition (https://www.kaggle.com/c/mens-machine-learning-competition-2019/data → click download all)
8. kaggle competitions download -c mens-machine-learning-competition-2019 (cmd function)
9. Unzip the downloaded zip file
10. Rename folder 'resources'
11. Clone this repository and place the resources folder in the newly cloned folder

# Exploratory Analysis
Exploratory Analysis.ipynb explores the data from kaggle and highlights a few key metrics used later for feature extraction. Also shows the average Pomeroy and Sagarin scores since 2003 (average = 70%). Data points include:

* Most tourney wins since 1985
* Conference with most wins
* Seeds with most titles
* Seeding Performance in the tourney (each round)
* Higher seeds winning percentage through the season
* Pomeroy/Sagarin Ranking
* Relationship between winning margin and ranking difference
* Averages (points per game, possessions per game, three pointers made and attempted, average free throws made and attempted, average assists, average defensive records)
* Advanced Stats (Possessions, Offensive Rating, Defensive Rating, Strength of Schedule, Performance Impact Estimator (PIE), Team Impact Estimator (TIE), Assist ratio, Turnover ratio, True Shooting %, Effect FG%, Free Throw Rate, Offensive Rebound %, Defensive Rebound %, Total Rebound %)
* Tournament vs Regular Season Stats (Points,Field Goals,Rebounds,)
* Statistics and wins (Field Goal Attempts, Field Goals made, Threes made, Free throws made, Free throws attempted offensive rebounds, defensive rebounds, blocks, steals, possessions, turnovers, personal fouls)

# Preprocessing Steps: 
Data Preparation.ipynb utilizes Pandas and NumPy to combine and clean the vase data sets. Then, creates a feature extraction model with Seaborn to highlight the most revelant features from the cleaned data set. Uses these features to create multiple classification models (Random Forest, Logistic Regression, Artificial Neural Network). Then creates a Confidence Score for each prediction made utilizing a KMeans clustering model. Finally, creates an Updset Score for each matchup utilizing a KMeans clustering model. 

# Creating a Prediction Bracket
MarchMadnessSimulator.ipynb creates a prediction bracket with the 64 teams in the March Madness Tournament (also includes the preliminary rounds). Contains the capability to output the prediction bracket as a PNG image.


