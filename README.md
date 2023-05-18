# EPL-Prediction
This project aims to predict the final point standings for all teams in the English Premier League for the 2022-2023 season. By analyzing the current performance of the teams that can determine the potential winner, the teams finishing in the top 4 or top 6, based on their performance.

To predict the winner, the current season's performance and the historical performance of the teams from previous seasons were considered. Analyzing the points earned from previous seasons and the factors that influence points, such as xG stats (expected goals) and offensive performance indicators, can make accurate predictions. In future projects, it would be beneficial to include pressing stats as they play a significant role in a team's overall performance. I began by scraping data from the FBRef website, where we gathered the necessary statistics for our prediction. The scraping process is divided into four steps, with a substantial time delay of 10 seconds between each step to ensure that FBRef does not ban our access for an extended period. 

Main Stats:
- xG: Expected goals.
- xGA: Expected allowed goals.
- Poss: Ball possession.
- GF: Goals scored.
- GA: Goals allowed.

Shooting Stats:
- Sh: Total number of shots.
- SoT: Shots on target.
- Dist: Average distance (in yards) from goal of all shots taken.
- FK: Shots from free kicks.
- PK: Penalty kicks made.
- PKatt: Penalty kicks attempted.

Passing Stats:
- KP: Passes that directly lead to a shot.
- 1/3: Completed passes that enter the final third of the pitch during offense.
- PPA: Completed passes into the 18-yard box, excluding set pieces.
- CrsPA: Completed crosses into the 18-yard box.
- Prog: Progressive passes, completed passes that advance the ball towards the opponent's goal by at least 10 yards from its furthest point in the last six passes, or any completed pass into the penalty area.

Possession Stats:
- Att 3rd: Touches in the attacking third of the pitch.
- Att Pen: Touches in the attacking penalty area.
- Prog: Progressive passes received, completed passes that advance the ball towards the opponent's goal by at least 10 yards from its furthest point in the last six passes, or any completed pass into the penalty area.

Goal and Shot Creation Stats:
- SCA: Shot-creating actions, the two offensive actions directly leading to a shot, such as passes, dribbles, and drawing fouls.

Pass Type Stats:
- TB: Completed pass sent between back defenders into open space.

To perform the prediction, I have five data frames containing fixtures for each team in the current season and the previous five seasons. The objective is to calculate the average features for each team in each season. For example, I determine the average xG per game or the average number of passes into the final third during a season. I have created a "season" function that generates a data frame with average features for each team in a specific season. I obtain a comprehensive dataset by merging these tables for the five seasons. The majority of features show a strong correlation with the number of points. While goals scored and allowed obviously influence wins, goal creation stats like xG, KP, Prog, and PPA significantly correlate with points, which is crucial for our prediction.

The overall prediction remains consistent, with Arsenal projected to finish first with over 89 points. Newcastle consistently secures the third position due to their strong performance statistics in the current season. It is worth noting that teams like Chelsea and Manchester United fare poorly in the prediction due to their lower performance indicators, despite their higher positions than Brighton and Liverpool in the current stage of the season. This could be attributed to Arsenal and Newcastle overachieving in terms of points at this stage of the season. Additionally, Arsenal's impressive performance averages, nearing championship-level per game statistics, coupled with their existing points, contribute to their predicted title win.

In future simulations, incorporating pressing quality statistics could enhance the accuracy of predictions. Teams like Manchester City, known for their exceptional pressing quality, might emerge as the champions in such simulations.
