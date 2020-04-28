# Assignment 3

## Does paying Lebron James more money increase his performance?

There's long been a debate about whether professional athletes actually earn the money they are paid. As the the salary caps for the United States' professional sports leagues have ballooned over past couple decades, has it actually made athletes' performances any better?

To explore this question, we'll use Lebron James, one of the greatest basketball players ever, as a case study. In evaluating if increasing the salaries of players improves performance, we'll consider a few key statistics in basketball. Among them, win percentage and effective field goal percentage. Obviously basketball is a team sport, and that's why I felt it was important to include effective field goal percentage in this discussion, as it is a truly individual statistic.

Also, it's important to consider that these statistics do not take several important variables into account. For example, how did James' performance differ between playing at his home arena and on the road? What time did the game start? How many days in row had he played? How far did the team have to fly before playing? These are all things that I would like to know when making this evaluation.

The traditional statistics involved in making this evaluation are readily available from sources like basketball-reference.com and stats.nba.com. However, understanding travel time and distance would be much more complex. That would involve some significant work. For example, you'd have to track down the travel itineraries for James' teams for every road trip throughout his entire career. That would take a lot of time, but would be important for understanding the exact travel time and distance associated with roadtrips. A less exact approach would be to track the distance between the major airports in cities with NBA teams.

Understanding how many consecutive days James has played is simpler, but also time intensive. It involves flagging any games played back-to-back throughout his entire career.

###Initial Dataset

|Season |Team               |Lg |Salary     |W  |L  |W%  |PPG |eFG% |$/Game  |
|-------|-------------------|---|-----------|---|---|----|----|-----|--------|
|2003-04|Cleveland Cavaliers|NBA|$4,018,920 |35 |47 |42.7|20.9|0.438|$49,011 |
|2004-05|Cleveland Cavaliers|NBA|$4,320,360 |42 |40 |51.2|27.2|0.504|$52,687 |
|2005-06|Cleveland Cavaliers|NBA|$4,621,800 |50 |32 |61  |31.4|0.515|$56,363 |
|2006-07|Cleveland Cavaliers|NBA|$5,828,090 |50 |32 |61  |27.3|0.507|$71,074 |
|2007-08|Cleveland Cavaliers|NBA|$13,041,250|45 |37 |54.9|30  |0.518|$159,040|
|2008-09|Cleveland Cavaliers|NBA|$14,410,581|66 |16 |80.5|28.4|0.53 |$175,739|
|2009-10|Cleveland Cavaliers|NBA|$15,779,912|61 |21 |74.4|29.7|0.545|$192,438|
|2010-11|Miami Heat         |NBA|$14,500,000|58 |24 |70.7|26.7|0.541|$176,829|
|2011-12|Miami Heat         |NBA|$16,022,500|46 |20 |56.1|27.1|0.554|$195,396|
|2012-13|Miami Heat         |NBA|$17,545,000|66 |16 |80.5|26.8|0.603|$213,963|
|2013-14|Miami Heat         |NBA|$19,067,500|54 |28 |65.9|27.1|0.61 |$232,530|
|2014-15|Cleveland Cavaliers|NBA|$20,644,400|53 |29 |64.6|25.3|0.535|$251,761|
|2015-16|Cleveland Cavaliers|NBA|$22,971,000|57 |25 |69.5|25.3|0.551|$280,134|
|2016-17|Cleveland Cavaliers|NBA|$30,963,450|51 |31 |62.2|26.4|0.594|$377,603|
|2017-18|Cleveland Cavaliers|NBA|$33,285,709|50 |32 |61  |27.5|0.59 |$405,923|
|2018-19|Los Angeles Lakers |NBA|$35,654,150|37 |45 |45.1|27.4|0.56 |$434,807|
