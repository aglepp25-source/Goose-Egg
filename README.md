# Goose-Egg

# I

My group consisted of myself and Nate Petz.

# II

The code from the Google Colab worksheet can be found in goose_eggs.py

# III

Introduction:
From 538, we found a dataset that creates a new stat for relief pitchers in the MLB known as a Goose Egg. It provides a dataset consisting of Goose Egg stats for every pitcher season up to the 2017 season, and the methodology for how it was calculated. 

Part of our analysis consisted of extending this dataset from the 2017 season up to the current 2025 season based off of MLB play by play data we found on retrosheets.com.

The second part of our analysis was comparing it to fastball velocity. From Statcast, which began tracking fastball velocity in 2015, we compared our Goose Egg totals to fastball velocity for each pitcher from 2015-2025. Broadly speaking, our goal was to analyze if there was a relationship between Goose Eggs and fastball velocity.

Methods and Results:
In the 538 article that initially described Goose Eggs, it provided what qualified as a Goose Egg. A Goose is defined as a high leverage appearance where the relief pitcher doesn’t lose the lead, or allow a run in the case of a tie game. Because a Goose is something rigidly defined in the play by play data, with the help of Gemini, we were able to create a new dataset in a Colab file that created Goose Egg statistics for the 2018-2025 seasons, and then integrated that with the 538 dataset.

The next step was importing fastball velocity data from Statcast, which was done through downloading the fastball velocity by percentile data. It was formatted so 100 would represent the fastest fastball while 0 would represent the slowest. We then on a scatterplot graphed fastball velocity against Goose Eggs for each season 2015-2025 to create our visualization. We also added a line of best fit so we could see if there was a correlation.

Here are the plots for the relevant seasons.



Conclusions:
As evidenced by the line of best fit, there appears to be a positive correlation between fastball velocity percentile and number of Goose Eggs. With the exception of the 2020 season, likely due to its small sample size due to a reduced regular season because of COVID, the line of best fit, and the error bars are trending positive for each season. This is important, because it indicates that a faster fastball is correlated with a higher number of Goose Eggs. This is interesting because it doesn’t control for the style of pitcher or number of fastballs pitched. It only mentions fastball velocity, so a pitcher with a relatively slow fastball, but doesn’t use it much is treated the same as a pitcher with a relatively slow fastball that uses it heavily. 

Another interesting takeaway is that in every season, there are many outliers from the line of best fit across the fastball velocity spectrum. There are many pitchers who overperform what their fastball velocity says, just as there are many pitchers who underperform. It is important to note that this only takes into account accumulated Goose Eggs, not rate of Goose Eggs, such pitchers who appeared less, for whatever reason, will have less Goose Eggs. It would be interesting to see if a similar correlation appears when comparing Goose Egg Percentage (number of goose eggs/maximum number of goose eggs) to fastball velocity percentile.

