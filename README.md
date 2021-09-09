# Football Data Visualizations
Hello ! In this repository I'll be uploading python files I created for as the title suggests football data visualizations, some example being player shot maps, pass maps, action maps and many others.

## [Scraping UnderStat Shot Data](https://github.com/yashrajOjha/football-data-viz/blob/main/Scraping%20Understat%20Data.ipynb)
For any visualization you always need data, this python file has the code to scrap data from Under Stat, a site where you will find detailed xG statistics for the top European leagues.

In our case, we will scrap shots data of Real Madrid vs Betis - La Liga 21/22. Firstly we parse the website data using Beautiful Soup, basically extract data from 'script' tags in the website. This raw data is then cleaned and loaded up as json. After that I create lists to store values like, the team Name, X and Y coordinates of the shot, result, expected goals and situation.

The lists are then converted to a dataframe using pandas, which is later converted to a CSV file for future reference.

## [Shot Map](https://github.com/yashrajOjha/football-data-viz/blob/main/Shot%20Map.ipynb)
Here for the shot map I've used the example of Andre Silva's 20/21 season for Eintracht Frankfurt. I collected his shot location, plotted it according to varying xG, meaning a shot with lesser xG will have a lower radius point and a shot with higher xG will have a bigger radius point. I further highlighted it according to the type of shot, a left/right foot shot or a header. 

The pitch was drawn with the help of mplsoccer, a python library helpful in different football vizzes.

The CSV file is processed by the help of pandas and the points are plotted using scatter plot from matplotlib.

## [Action Map](https://github.com/yashrajOjha/football-data-viz/blob/main/Action%20Map.ipynb)
Action Map is used depict what kind of action a player is performing on the field, a dribble/takeon, an interception, a tackle and so on. Similar to the shot map I've used the mpl soccer library for drawing the pitch. Every action from the player is represented in different color and shape, and is implemented using scatter plot from matplotlib.

The CSV file has player name, event, x and y position and is processed as a data frame using pandas.

## [Pass Map](https://github.com/yashrajOjha/football-data-viz/blob/main/Pass%20Map.ipynb)
Pass Map shows us the passes a player made during a match, in this CSV file I've categorized the passes as successful and unsuccessful, with the former being indicated by green and the latter red. The passes have a set of four coordinates, start x, start y which locate the starting coordinates of the pass and end x, end y which locate the ending coordinates of the pass. The starting coordinates indicated by a point using the scatter plot feature and the 4 points are connected together using the plot feature of pyplot.

## [Heat Map](https://github.com/yashrajOjha/football-data-viz/blob/main/Heat%20Map.ipynb)
Heat Map depicts regions in which a player oftenly operates. We identify the region of operation by mostly highlighting the starting points of passes/actions, in our case it is passes.

Libraries used are SciPy for filters, Cmasher for colors, MPLSoccer for the pitch, Pandas to process data and MatPlotLib for plotting the points. 

In code: bin_statistic: divides the space into bins, and returns the count of the number of passes in each bin. In our example the pitch is divided into 25 x 25 bins, bins that have a higher number of starting pass points are highlighted by more vibrant colour. 
The Gaussian filter is used as a smoothing operator, used to 'blur' images and remove detail and noise.

## [Stacked Horizontal Bar Graphs](https://github.com/yashrajOjha/football-data-viz/blob/main/H%20Bar%20Graph%20(21-22%20LaLiga%20Transfers).ipynb)
This graph depicts the type of transfers made by La Liga teams in 21/22 {Real Madrid, Barcelona, Atletico, Villarreal, Sevilla}. The transfer types are {sold, bought, loan-in, loan-out} highlighed in different colors using options from cmasher.

## [Comet Style Glowing Pass Maps](https://github.com/yashrajOjha/football-data-viz/blob/main/Comet%20Pass%20Maps.ipynb)
This style of pass maps was inspired by the one available with MPL Soccer. The basics are the same as normal pass maps, but here the lines have a glow and the endpoint of passes are shown as comets. Just like normal pass maps the pitch is drawn with the help of MPL Soccer library, the type of passes are shown by different colors.

The glow in the passes and lines are done using another loop that plots the line with a low alpha (transparency) value and gradually increases the linewidth.

## [Scatter Plot](https://github.com/yashrajOjha/football-data-viz/blob/main/Hardworking%20FWs%20in%20MLS.ipynb)

This is a scatter plot to show the hardworking forwards in the MLS, I've used pressures as the metric, Number of pressures p90 in the Middle 3rd on the Y axis and number of pressures p90 in the Attacking 3rd on the X axis, the plot has a filter, which is the player should have played more than 9.0 90s. I've shown names of the players that have above average pressure stats (I intend on altering the text placement in the future).
