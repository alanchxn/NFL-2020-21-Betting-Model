# NFL 2020-21 Betting Model

As someone who enjoys betting on sports in my spare time, I decided to create a model that calculates the expected point margin (or spread in betting terms) of any two NFL teams using Linear Regression and key statistics that contribute to wins. 

The statistics used are:
- SRS (Simple Rating System)
  - A rating that takes into account average point differential and strength of schedule. The rating is denominated in points     above/below average, where zero is average.
- DVOA (Defense-adjusted Value Over Average)
  - Calculates a team's success based on the down-and-distance of each play during the season, then calculates how much more or less successful each team is compared to the league average.
- Differential
  - Point differential throughout the season
- ATS%
  - A team's ability to "cover the spread" or win my more than the expected margin as determine by Vegas odds
- CG% 
  - A team's ability to win "close games"; games that are decided by 1 possession or less (7 points)
  
- Back-end testing still in progress
- Continuing to update model
- Looking at add more advanced analytics
