# Project | FIFA21 game.
## Predicting players' overall rating (OVA).

We were given a dataset consisting of data of players of FIFA21 game.

This data included:
- **Personal information** of the player (id, name, nationality, club, height, weight, value, wage, etc.),
- The **attributes** of the player (measures of how the player passes, shoots, dribbles, runs, jumps, tackles, etc.),
- The player's **best position** and **main positions** (for example, GK, CF, CM, LW, etc.).
- A measure of **how the player performs when not in its best position or main positions**.
- The **international reputation** of the player (IR, ranging from 1 to 5).
- Other information (like performance with weak foot or skill moves).
- **OVA**. The overall rating of the player's capacity to perform in the game.

### **Objective**. Our goal is to build a **linear regression model** that predicts as best as possible the **OVA**.


## 1. Understanding the data and making decisions.
Our first priority is to understand the data we're dealing with. We first take a look at the information in the dataset.
We use our knowledge of the videogame and also information on the web that offers descriptions of the OVA and its components.

We finally come to understand that the OVA is mainly obtained with the following formula:

  ```**OVA = Atttributes + IR (international reputation).**```

Depending on the position the player plays in, the model takes into account different attributes:

<div align="center">
  <img src="https://github.com/92CMDiego/Project_FIFA21/blob/main/GK.jpg?raw=true" alt="" width="150">
  <img src="https://github.com/92CMDiego/Project_FIFA21/blob/main/CDM.jpg?raw=true)" alt="" width="200">
  <img src="https://github.com/92CMDiego/Project_FIFA21/blob/main/STRIKER.jpg?raw=true" alt="" width="180">
</div>

We also need to take into account a value in the dataset that modifies the rating of the player when the player plays in different positions.


So we're going to need the second number that appears in these columns. We're going to split those values into two different columns and obtain the second value.

Our model will be built based on this **main assumption**:
    
**The OVA could be calculated with the values of the attributes, the international reputation and the +/- the player gets in the different positions.**

We'll define our model with the following features and target:
- **Numerical features**: **attributes** of the players, **international reputation** and **the + or - the player gets when in the different positions**.
(We exclude the columns that are a summation of other columns).
- **Categorical features**: **best position** of the player.
- **Target**: **OVA**.


## 2. Cleaning the data, preparing the data and building the model.
- We standardize the names of our columns (using "snake_case" convention).
- We encode our categorical feature (best position) with one hot encoder.
- We remove some of the symbols that are inside the data of our numerical features.
- We replace "na" values that we encounter for some attributes with the mean of the values of that column.
- We check the correlation bewteen numerical features and the target and discard the ones with a correlation of less than 0.2 with the target.
- We normalize our numerical features with MinMaxScaler.
- We do a train-test split with a value of 0.1 for the size of the test data.
- We fit our linear regression model.
- We obtain the following metrics. R2 score (train): . R2 score (test): . MAE: . MSE: . RMSE: .

## 3. Validating the performance of the model wiht a new dataset.
The next day we are given a new dataset. The format of the information is the same but it contains new individuals (new data).
We use this new data to validate how the model performs.
We obtain the following metrics. R2 score: . MAE: . MSE: . RMSE: .

## 4. Improving the model.
We try different changes in the model. Our final model contains the following changes:
- We don't discard any of the features because of low correlation.
- We include a new numerical feature: "wage".
- We obtain the following metrics. R2 score: .  MAE: . MSE: . RMSE: .

##### Links of visited sites.
- Explanations of the acronyms and abbreviations: (https://gaming.stackexchange.com/questions/167318/what-do-fifa-14-position-acronyms-mean).
- Explanations of the acronyms and abbreviations: (https://fifauteam.com/fifa-ultimate-team-positions-and-tactics/).
- FIFA 19 player rating guide (https://fifauteam.com/player-ratings-guide-fifa-19/).
- FIFA overall rating explained (https://earlygame.com/fifa/fifa-ratings-explained-overall-rating).
- FIFA 21 all attributes divided (https://fifauteam.com/fifa-21-attributes-guide/).
