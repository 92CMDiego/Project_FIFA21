# Project_FIFA21

We were given a dataset consisting of data of players of FIFA21 game.
This data included:
- Personal information of the player (id, nadme, nationality, club, height, weight, value, wage, etc.),
- The attributes of the player (measures of how the player passes, shoots, dribbles, runs, jumps, tackles, etc.),
- The player's best position and main positions.
- A measure of how the player performs when not in its best position or main positions.
- The international reputation of the player.
- Other information (like performance with weak foot or skill moves).
- OVA. The overall rating of the player's capacity to perform in the game.

Objective. Our goal is to build a linear regression model that predicts as best as possible the OVA.


## 1. Understanding the data andd making decisions.
Our first priority is to understand the data we're dealing with. We first take a look at the information in the dataset.
We use our knowledge of the videogame and also information on the web that offers descriptions of the OVA and its components.

After having a deeper understanding of the , we take a closer look at the dataset we are given. We derive some conclusions and make some decisions:



## 2. Cleaning the data and building the model.
- We standardize the names of our columns (using "snake_case" convention).
- We encode our categorical feature (best position) with one hot encoder.
- 


## 3. Validating the performance of the model wiht a new dataset.


## 4. Improving the model.


##### Links of visited sites.
- Explanations of the acronyms and abbreviations: (https://gaming.stackexchange.com/questions/167318/what-do-fifa-14-position-acronyms-mean).
- Explanations of the acronyms and abbreviations: (https://fifauteam.com/fifa-ultimate-team-positions-and-tactics/).
- FIFA 19 player rating guide (https://fifauteam.com/player-ratings-guide-fifa-19/).
- FIFA overall rating explained (https://earlygame.com/fifa/fifa-ratings-explained-overall-rating).
- FIFA 21 all attributes divided (https://fifauteam.com/fifa-21-attributes-guide/).
