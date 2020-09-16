### Business Problem 

My Hypothesis is that the winning team prediction depends on the players batting & bowling profile.

In this notebook, I create player profile using 2 tables 1) Matches table 2) Deliveries table

Matches table has match information from season 2008 upto season 2019 Deliveries table has ball to ball delivery information from season 2008 to season 2017

So, I created player profile using deliveries information of season 2008 upto season 2016 and tried to validate my hypothesis on season 2017 matches.

**End Result** : My hypothesis doesnt hold true when looked for 5 matches. So our hypothesis that the winning team prediction depends on player profile cannot be used to predict 2020 winners


**Key Points from the analysis**

1) New players - there wont be a profile of a player if he didnot play in any season

2) Players whose dismissal is equal to 0 i.e who where not out in the game will have infinite in 'Calc' column.When further looked into such players profile they turn out to be bowlers or batsman whose batting order is 10th or 11th position.So we excluded such players while calculating the batting order of a team


Dataset :https://www.kaggle.com/saiharsha1234/ipl-prediction-1st-hypothesis . Tools used : Python Libraries used : pandas, numpy

## Batting Data Dictionary

1)Batsman name

2)Batting_played - No of matches where a batsman played

3)Player_dismissed(outs) - No. of matches where a batsman was out

4)Total_runs(TR) - Total runs scored by a batsman in all the matches

5)HS(Highest score) - Highest runs in a match by a batsman

6)Ballsfaced(BF) - No. of balls faced

7)4's - Count of 4's

8)6's - Count of 6's

9)Avg(TR/M):Total runs/matches

10)SR(TR/BF): 100 * Total runs/Balls faced

11)battingAVG(TR/outs):Total runs/Player dismissed

12)runs_by_balls(R/B):Total runs/Balls faced = StrikeRate/100

13)Calc - battingAVG * runs_by_balls

## Bowling Data Dictionary

1)bowler name

2)matches - No of matches bowled by a bowler

3)BallsBowled - Total Balls Bowled by a bowler in all the matches

4)wkts - Total No. of wickets taken by a bowler in all the matches

5)Runs - Total No. of runs given by a bowler in all the matches

6)Avg(TR/Wkts):Total runs/wickets taken

7)bowling_sr(bb/wkts):Balls Bowled/wickets taken

8)economy_rate(runs/bb):Runs given by bowler/Balls Bowled

13)CombinedBowlingRate - 3/(1/Avg+1/bowling_sr+1/economy_rate)
