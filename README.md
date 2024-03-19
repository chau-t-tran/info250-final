# NBA Defensive Kings - What Are The Historical Trends?

![example](https://github.com/chau-t-tran/info250-final/blob/main/cumulative.PNG?raw=true)

## Visualization Link

https://public.tableau.com/app/profile/chau.tran8335/viz/NBADefensiveStats/Dashboard1

## Introduction

In an age of NBA basketball where the highlights are often slam-dunks, clutch 3s from deep, and ankle-breakers, it seems like defensive prowess often gets overlooked. We can see this reflected in the basketball community as well. Many "old-heads" will claim that the way basketball was played in the 90's and 80's was much tougher and grittier and that the current generation is "soft". Perhaps we can get a glimpse of this perspective by looking purely at the defensive stats from historical NBA basketball data.

## Research Questions

If by "toughness" we mean defensive prowess, we can filter through the data in the NBA history books to understand how defense has evolved over the years and what the top defensive players in NBA history looked like.

The average viewer of this visualization may have the following research questions:

* How does height play a role in the number of total rebounds a player grabs throughout their career?
* Additionally, who were the outliers in this height-rebound relationship? i.e., who were the short players
who grabbed a lot of rebounds throughout their careers?
* How does the quantity of steals change over the course of the 67 years that the dataset covers?
* Who were the top 5 players with the most career blocks in history?
* Who were the top 5 players with the most career blocks in history who were 6’4” and under (usual size
for a point guard and point guards are typically not known for blocking)?
* Who was the greatest in their respective role (PG, SG, SF, PF, C, etc.)
* Who were the outliers throughout basketball history - for example, who was the greatest rebounder,
who always grabbed the most steals each game, etc.
* ...etc.

## Dataset Details

The dataset used is one last updated in 2017 grabbed from Kaggle:

https://www.kaggle.com/datasets/drgilermo/nba-players-stats/data

The dataset contains every NBA players' seasonal stats each year starting in the 1950s until the 2017s.
It contains all offensive and defensive statistical fields in addition to the advanced box-score metrics added
as NBA statistical tracking evolved over the years.

This dataset comes in two major parts:
* **Player Data**, which contains player names, height, weight.
* **Seasonal Data**, which contains the actual players' box-scores.

Both of these tables are linked together via a composite key of the player name concatenated with their height.
This is because in NBA history, there are players with the same name - however, among this subset of players, none
of them had the same height. Thus, name+height seemed to serve as a good primary key.

Note that there may be some missing data in this dataset - especially for older data. This is because when the NBA
first started in the 1940's, only basic box-scores were kept track of: points, assists, free throws, etc. Only
over time did the NBA begin adding more metrics:

* Rebounds: 1950-1951
* Minutes: 1951-1952
* Games Started: 1970-1971
* Steals: 1973-1974
* Blocks: 1973-1974
* Off Rebounds: 1973-1974
* Def Rebounds: 1973-1974
* Turnovers: 1977-1978
* 3 Point Field Goals: 1979-1980

However, to not include the older, but less detailed data, would be to ignore some of the defensive
beasts that existed in the days of yore - such as Wilt Chamberlain and Bill Russell.

## Visualization Methods 

The Tableau visualization provides 5 different ways of browsing through the defensive side of NBA history:

* **Cumulative Per Game**: The x-axis is the player height. The y-axis is the rebounds,
blocks, and steals depending on what tab the user is on. More specifically, the user is able
to switch views via tabs to view block data vs. steals data vs. rebound data in order to avoid
cognitive overload.
* **Percentage Per Game**: Very similar to the above scatter plot, except this will
display rebound percentage, block percentage, and steal percentages. Additionally, there will
be an interactive range filter (documented in this link) to filter out players that follow below a
threshold of number of rebounds, blocks, steals, height and weight. This is so that the user can
disregard players who only blocked one or two times a season but have a block percentage of 100%
and also answer the question of who the best short defensive players were.
* **Leaguewide Per Game Stats**: The x-axis is the year representing the corresponding NBA season. The y-axis will
be the average rebounds, blocks, and steals LEAGUE-WIDE. Users is able to follow the
trends of each statistic throughout history.
* **Defensive Stars Seasonal**: Additionally, having a line chart of INDIVIDUAL rebounds, blocks
and steals of the all-time league leaders in rebounds, blocks, and steals would also be interesting
from a user point of view. For example, given some subset of historical all-time defenders, we
graph on the x-axis how many years into their career and on the y-axis a filterable view of seasonal
rebound, blocks, and steals (again, separating with different tabs). From this, the user can see
where in a defenders career does their rebounds, blocks, and steals usually peak (early in their
career when they are still athletic, or late in their career when they are more experienced, etc.).
* **Defensive Stats Individual Player Search**: The user is able to view the individual defensive stats of any player of their choice. This allows them to go into deeper detail of a particular player rather than just a broad overview of league-wide data.

## Results
![rebounds](https://github.com/chau-t-tran/info250-final/blob/main/rebounds.PNG?raw=true)

What is most interesting to see is in the **Leaguewide Per Game Stats** visualization, which depicts defensive treds over the years. It seems that the 3 core defensive stats - rebounds, blocks, steals - have ALL decreased over the years from 1973-2017. 

One can argue that the defense has gotten lazy over the years and that modern players do not have the same metal as in the past. However, it can also be argued that NBA offense has simply outpaced defense in the modern era.

It turns out that to truly see the full picture, we need to view both sides of the coin - defensive and offensive stats and how the two aspects of basketball has evolved over the years.

## Conclusion

Throughout the semester, I feel that I've learned a lot about how important _interactive_ data visualization is - evident by how many sliders and knobs I have added to this final project. As a software engineer with little experience in data science and data visualization, the extent of my visualizations when presenting have been limited to just graphs and tables on a static PowerPoint slide - which seems to have work okay so far. However, I think when conveying complex ideas is the goal, these more in-depth interactable visualizations leave a better idea and a more lasting impression on clients.
