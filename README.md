Data Visualization is an important aspect of working with datasets.

## Basic example of data visualization:

Some libraries most commonly used:
Pandas, Matplotlib, Seaborn

### Begin by importing the libraries
     ```
     import pandas as pd
     import seaborn as sns
     import matplotlib.pyplot as plt
     ```
### Usually you're working with a dataset, bring it to the Pandas DataFrame
     ```
     iris = pd.read_csv(<filepath>/input/<filename>.csv)
     iris.head()
     ```
     
     Important to note, the `head()` command is used to inspect a portion of your data
     
### How to inspect the number of species in your data you have so far
     ```
     iris["Species"].value_counts()
     ```

### Next is some actual categorization of the data that we have
Below code produces a scatter plot with legends of the sepal length versus the sepal width on the x and y axes respectively
     ```
     iris.plot(kind="scatter", x="SepalLengthCm", y="SepalWidthCm")
     ```

## Additinal information
Customizing your marker types and details:

Creating the plot object:
     ```
     ax = plt.subplots()
     ax.scatter(x_data, y_data, s = 10, color = color, alpha = 0.75)
     ```
What did this do? Create a plot object, designate it to be a scatter plot, set the size and transparancy of the marker, the alpha.

Other marker-related distinguishing types:
     ```
     for marker in['o', '.', ',', 'x', '+', 'v', '^', '<', '>', 's', 'd']:
     plt.plot(rng.rand(5), rng.rand(5), marker, label = "marker = '{0}'".format(marker))
     'o' = circle marker
     '.' = small dot marker
     ',' = exceptionally small dot marker
     'x' = x marker
     '+' = plus marker
     'v' = downward facing triangle marker
     '^' = upward facing triangle marker
     '<' = leftward facing triangle marker
     '>' = rightward facing triangle marker
     's' = square marker
     'd' = diamond marker
     ```
## This was applicable for a scatter plot example. There are other types of graphs like bar graphs which will be in the next update.

     
