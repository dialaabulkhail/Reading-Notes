# Seaborn 
Seaborn is a Python library based on matplotlib, it provides an interface for drawing attractive and informative statistical graphics.

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
