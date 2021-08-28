# Football Data Visualizations
Hello ! In this repository I'll be uploading python files I created for as the title suggests football data visualizations, some example being player shot maps, pass maps, action maps and many others.

## Shot Map 
Here for the shot map I've used the example of Andre Silva's 20/21 season for Eintracht Frankfurt. I collected his shot location, plotted it according to varying xG, meaning a shot with lesser xG will have a lower radius point and a shot with higher xG will have a bigger radius point. I further highlighted it according to the type of shot, a left/right foot shot or a header. 

The pitch was drawn with the help of mplsoccer, a python library helpful in different football vizzes.

The CSV file is processed by the help of pandas and the points are plotted using scatter plot from matplotlib.

## Action Map
Action Map is used depict what kind of action a player is performing on the field, a dribble/takeon, an interception, a tackle and so on. Similar to the shot map I've used the mpl soccer library for drawing the pitch. Every action from the player is represented in different color and shape, and is implemented using scatter plot from matplotlib.

The CSV file has player name, event, x and y position and is processed as a data frame using pandas.

## Pass Map
Pass Map shows us the passes a player made during a match, in this CSV file I've categorized the passes as successful and unsuccessful, with the former being indicated by green and the latter red. The passes have a set of four coordinates, start x, start y which locate the start coordinate of the pass and end x, end y which locate the ending coordinates of the pass. The starting coordinates indicated by a point using the scatter plot feature and the 4 points are connected together using the plot feature of pyplot.
