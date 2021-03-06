# NFL 2020-21 Betting Model

### Introduction
As someone who enjoys betting on sports in my spare time, I decided to create a model that calculates the expected point margin (or spread in betting terms) of any two NFL teams using Linear Regression and key statistics that contribute to wins. 

### Key Statistics
- **SRS** (Simple Rating System)
  - A rating that takes into account average point differential and strength of schedule. The rating is denominated in points     above/below average, where zero is average.
- **ATS%**
  - A team's ability to "cover the spread" or win my more than the expected margin as determine by Vegas odds
- **Differential**
  - A team's point differential throughout the season
- **DVOA** (Defense-adjusted Value Over Average)
  - Calculates a team's success based on the down-and-distance of each play during the season, then calculates how much more or less successful each team is compared to the league average.
- **CG%**
  - A team's ability to win "close games"; games that are decided by 1 possession or less (7 points)

### Build Status
- Back-end testing still in progress
- Continuing to update model
- Looking to add additional key metrics/statistics

### How to use?
- The model is based off of how many teams the home team should yield to the away team for the game to be fair. 
- In the **Bet Tracker** tab under the **Model Prediction** column, there are three examples of the home team being yielded that number of points. 
  - For example, in the first game, the Chiefs should be *getting* approximately **0.36** points at home for it to be a fair game against the Bills. In the second game, the Packers should get **2.52** points against the Bucs, and in the third game the Chiefs should be *giving away* **18.34** points, meaning that a 50/50 bet on the Chiefs should mean that they win the game against the Jets by **18.34** points or more.
- To use this model for any two teams:
  1. Copy paste each team's SRS, DVOA, Differential, ATS%, CS%, and Y/A in two seperate rows.
  2. Then, set a formula in column k that equals (where the italicized portions are the coffefficients on the left hand side)
       = *Intercept* + (*hSRS* * ```home team SRS```) + (*hDVOA* * ```home team DVOA```) + (*hATS%* * ```home team ATS%```)+ (*hCG%* * ```home team CG%```) + (*hY/A* * ```home team Y/A```) + (*aSRS* * ```away team SRS```) + (*aDVOA* * ```away team DVOA```) + (*aATS%* * ```away team ATS%```)+ (*aCG%* * ```away team CG%```) + (*aY/A*) * ```away team Y/A```)

### Screenshots in Action
![Screen Shot 2021-01-18 at 1 54 21 AM](https://user-images.githubusercontent.com/44907256/104882159-90593600-5930-11eb-988a-22c3bc2f516b.png)
- Overview of the Linear Regression Model

![Screen Shot 2021-01-18 at 2 03 32 AM](https://user-images.githubusercontent.com/44907256/104882655-6b18f780-5931-11eb-9259-300650cc169a.png)
- Bet tracker, including a couple of examples for reference

![Screen Shot 2021-01-18 at 1 53 45 AM](https://user-images.githubusercontent.com/44907256/104882367-fba30800-5930-11eb-90c5-e25706781f9a.png)
- The stats used for this model associated with each team

![Screen Shot 2021-01-18 at 1 53 29 AM](https://user-images.githubusercontent.com/44907256/104882371-fcd43500-5930-11eb-9c25-e397c25e8f7e.png)
- SRS Rating of each team

