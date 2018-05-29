
install.packages("tidyverse")   # To install the tidyverse package
library(tidyverse)   # To load library tidyverse

install.packages(c("nycflights13", "gapminder", "Lahman")) # To install the listed data packages

##########################################################################################
# I. EXPLORE
# ***********
# This section in the book deals with various aspects of data exploration.
# Accoridng to the author, data exploration is the art of looking at the data,
# rapidly generating hypotheses, quickly testing them, then repeating these 
# steps again and again. Data exploration makes one familiar with the data and
# thus helps you to ask questions and look for answers. It's goal is to find
# many promising leads that can be further explored.
#
#------------------------------------
# Cynthia Asingwa
# 14th May 2018
#-----------------------------------
#
# 3. Data Visualization
# *********************
# 
# Visualizing data using ggplot2
#-----------------------------------------------------------------------------------------


library(tidyverse)  # Loads library tidyverse
ggplot2::mpg    # Loads the dataframe mpg from ggplot2

# Creating a ggplot of displ (x-axis) against hwy (y-axis)

ggplot(data= mpg) +  # This alone, without the + creates an empty graph
  geom_point(mapping = aes(x = displ, y = hwy))  # Adds a layer of points

# "ggplot() creates a coordinate system that you can add layers to."
# Each geom function adds a different type of layer to a plot

# Conclusion from graph, cars with big engines have low fuel efficiency and thus consume
# more fuel. The relationship is negative.

# Each geom function takes a mapping argument which is always paired with aes() and the x and
# y arguments of aes(). 

dim_desc(mpg) #  Describes the dimension of the data frame

# Scatter plot of hwy vs cyl

ggplot(data= mpg) +
  geom_point(mapping = aes( x = hwy, y = cyl))

# Scatter plot of class vs drv

ggplot(data = mpg) +
  geom_point(mapping = aes( x = class, y = drv))


# One can adda third variable to a 2D scatter plot by mapping it into an aesthtic(aes)
# Aesthetics include size, shape or color
# Map the colors of the points to the class variable to reveal the class of each car

ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy, colour = class, size = cyl))

# ggplot slects a reasonable scale to use with the aesthetic and constructs a legend
# For x and y aethetics, it creates and axis line with tick marks and a label

# To set an aesthetic manually, set it outside of aes() as an argument of your geom fn

ggplot( data = mpg)+
  geom_point(mapping = aes(x=displ, y = hwy), colour = "orange")

# Manual aes values are as follows;
#  * for colour, the name as a character string
#  * for size of a point, in mm
#  * for shape, the number of the shape as in the figure shown in R4DS, between 1 to 25

# EXERCISE
# 1. The points are not blue since the argument for manual aesthetics is within the aes()
# 2. Categorical variables - manufacturer, model, trans, drv, fl, class
#    Continuous variables - displ
#    Click on dataframe name in Environment window, view(mpg) or str(mpg)

str(mpg) 

# 3.
ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy, colour = displ))

ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy, size = displ))

ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy, shape = displ))
# A continuous variable cannot be mapped to shape

# 4. Same variable, multiple aesthetics. 
ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy, colour = hwy, 
                           size =hwy, stroke = 5))

# 5. Stroke aesthetic, what does it do?
ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy,stroke = 2), shape = 17)

# 6. The points are divided into different colors for the evaluations True and False
ggplot(data = mpg)+
  geom_point(mapping = aes(x = displ, y = hwy, colour = displ <5))

#           Facets
#           *******
# A facet is a subplot that displays one subset of the data. It is especially useful
# when plotting categorical variables, such that, each category is plotted in its own
# subplot.

ggplot(data=mpg)+
  geom_point(mapping = aes(x=displ, y=hwy)) +
  facet_wrap(~ class, nrow=2)
# ~ is a formula, a data structure in R, and it is placed before the variable (likely categorical)

# You can facet the plot on a combination of two variables by using facet_grid()

ggplot(data=mpg) +
  geom_point(mapping = aes(x=displ, y=hwy)) +
  facet_grid(manufacturer ~ cyl)



# 3.5.1 Exercises
# 1. When you facet on a continuous variable
# You get as many grids as there are unique values of the variable.

ggplot(data = mpg) +
  geom_point(mapping = aes( x= cyl, y = hwy))+
  facet_wrap( ~displ)

#2. 













# library(tidyverse)

ggplot(data = mpg) +
  geom_point(mapping = aes(x = displ, y = hwy))

filter(mpg, cyl==8)
filter(diamonds, carat>3)



