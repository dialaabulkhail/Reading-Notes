# matplotlib Tutorial
matplotlib a pyhton package for 2D graphics provides a very quick way to visualize data from Python and publication-quality figures in many formats.

# Seaborn 
- Seaborn is a Python library based on matplotlib, it provides an interface for drawing attractive and informative statistical graphics.
- IPython is a python shell that provide features such as named inputs and outputs, access to shell commands, improved debugging.
>  It allows interactive matplotlib sessions that have Matlab/Mathematica-like functionality.

- pyplot provides a convenient interface to the matplotlib object-oriented plotting library.

Matplotlib comes with a set of default settings that allow customizing all kinds of properties like controlling figure size and dpi, line width, color and style, axes, axis and grid properties, text and font properties.. 

[More on matplotlib](https://github.com/rougier/matplotlib-tutorial/blob/master/README.rst)

## Overview of seaborn plotting functions

you can plot a seaborn graph
```
# Import seaborn
import seaborn as sns

# Apply the default theme
sns.set_theme()

# Load an example dataset
tips = sns.load_dataset("tips")

# Create a visualization
sns.relplot(
    data=tips,
    x="total_bill", y="tip", col="time",
    hue="smoker", style="smoker", size="size",
)
```

[seaborn tutorial](https://seaborn.pydata.org/tutorial.html)

[Seaborn cheat sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf)

# Binder - Bokeh
# overview
Bokeh isa library that provides a quick and easy interactive visualization of plots, dashboards and data applications

usage of Bokeh:
- Interactive visualization in modern browsers
- Standalone HTML documents, or server-backed apps
- Expressive and versatile graphics
- Large, dynamic or streaming data
- Easy usage from python
- no Javascript required.

[More on Bokeh](https://mybinder.org/v2/gh/bokeh/bokeh-notebooks/master?filepath=tutorial%2F00%20-%20Introduction%20and%20Setup.ipynb)
