# Readings: Data Visualization

 Data visualization is the graphical representation of information and data.
 
By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## [Matplotlib Tutorial](https://github.com/rougier/matplotlib-tutorial)

#### WHAT?

matplotlib is the single most used Python package for 2D-graphics. 

It provides both a very quick way to visualize data from Python and publication-quality figures in many formats.

We are going to explore matplotlib in interactive mode covering most common cases.

#### IPython

is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more.

#### pyplot

pyplot provides a convenient interface to the matplotlib object-oriented plotting library.

It is modeled closely after Matlab(TM).

**The first step is to get the data for the sine and cosine functions:**
```
import numpy as np

X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)

```

```
plt.figure(figsize=(10,6), dpi=80)
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
```

![matplot-tutorial](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_3.png)



## [Saborn](https://seaborn.pydata.org/tutorial.html)

Seaborn is a Python data visualization library based on matplotlib. 

It provides a high-level interface for drawing attractive and informative statistical graphics.

## [Bokeh](https://hub.gke2.mybinder.org/user/bokeh-bokeh-notebooks-3q7wvau0/notebooks/tutorial/00%20-%20Introduction%20and%20Setup.ipynb)

Bokeh is a Python library for creating interactive visualizations for modern web browsers. 

It helps you build beautiful graphics, ranging from simple plots to complex dashboards with streaming datasets.

With Bokeh, you can create JavaScript-powered visualizations without writing any JavaScript yourself.



[bokeh.org](https://bokeh.org/)
