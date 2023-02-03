# Data Visualization using Matplotlib

## Key Pointers:
1. Matplotlib is the most popular plotting library for python as it gives you control over every aspect of the plot/ figure
2. Other advanced libraries like seaborn as based on Matplotlib. 
3. It is well integrated with Pandas/Numpy
    -  All plotting functions expects NumPy array as input. Classes that are 'array-like' such as pandas data objects and NumPy matrix may or may not work as intended. It is best to convert these to array objects prior to plotting.
    - All the sequences are converted to NumPy array internally.
4. Matplotlib graphs your data on Figures, which contain one or more axes (axes: an area where points can be specified in terms of x-y coordinate  - it also allows the placement of the plots at any location in the figure).


## Approach of using Matplollib:
There are two ways of creating Matplotlib plots!

<b>Functional Approach:</b> Rely on pyplot to automatically create and manage the figures and axes, and use pyplot functions for plotting.
1. In functional approach, the collection of function from pyplot API makes some changes to the figure - like create a figure, add axes, plot lines, and other decoration to the plot
2. When we use the functional approach to plot, the figures and axes are created by default and all the calls are made on the current figure and axes
3. In pyplot (functional approach) various states are preserved cross function calls, so that it keeps track of things like the current figure and plotting area and all the functions are directed to the current axes
4. Pyplot API are generally less flexible than the Object Oriented API


<b>Object Oriented approach:</b> Explicitly create figures and axes, and call methods on them
1. The figure object is instantiated and then the methods and attributes are called on that object.
2. Although this increases a few steps, but it offers a lot more control over the plot. When we use the Object oriented approach we can control which figure and axes we want to work on. 
3. It is advisable to use Object oriented approach for actual codes (where you have other classes and objects).when handling multiple figures/axes, you will not get confused as to which one is currently active since every subplot is assign to an ax

## Parts of Matplotlib Figure:
1. Figure
    - is basically the entire canvas with axes (this is where you gonna put all the graphs and other elements like title, labels legends etc)
    - It can have any number of axes, but will typically have at least one.  if you have one plot on a figure, then that plot is the axes. If you have multiple subplots on a figure, then each subplot is one axes.
    - It is convenient to have axes created with Figure, but you can add axes to a figure later for complex axes layout.
2. Axes
    - Region of the image with the data space.
    - Contains: 2 axis objects - which take care of the data limits, title, and labels for both axis object
    - Most of the other charting objects are tied to an Axes - they can't be shared by Multiple Axes or moved from one to another.
3. Axis
    - They are number-line like objects. 
    - Take care of graph limit and generating ticks and tick labels. 
4. grid
5. Figure & Axes Titles
6. X & Y Labels
7. Legends
8. Major & Minor ticks and tick labels
    - The location of the tick is determined by the locator object
    - the tick label string is formatted by the Formatter
9. Vertical & Horizontal lines
10. Markers, Text and annotation

## Flow of working with object oriented approach for plotting the visual

1. Import the library
    - we would import the pyplot class from the package
2. Initiate the figure and axes objects:
    - You can either initate the figure object separately using plt.figure() objects and than add axes to the figure using fig.add_axes() or fig.add_subplot() or you can use plt.subplots() to create both of them simutaneously
    - With both these functions you can take a lot of parameters to customize the look and feel of the graph like: figure size, face color, edge color, width
    - You can insert plot in the same figure by adding another axes object in the same figure canvas. You can create different types of plots within the subplot
    - Subplot will delete any pre-existing subplot that overlaps with it beyond sharing a boundary.
3. Format the axes
    - Setting the limit, scale, spines, setting ticks and other similar itesm
5. Plot the graph
    - create the graph invoke plot() method on the axes object. Its a basic method of axes class which plots values of one array versus another as lines. 
7. Set Labels and titles
    - Set the labels and title including other settings - like color, size, alignment
9. Add Grid Lines and legends
10. Fit the chart
    -To fix any overlapping issues in the graph use
12. Diplay the final chart
