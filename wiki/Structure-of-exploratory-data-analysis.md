This is still work in progress, but it would be useful to have a framework of reference for any data exploration we attempt.
Sunny captured her approach in this blog post [here](https://witanblog.wordpress.com/2017/05/05/how-i-approach-analysing-a-data-set/).

### Steps

* **Describe (annotate)** what every field should contain, identify relevant fields
* **Summarize** the values:
  - for numerical fields: summarize (5 values), histogram
  - for categorical fields: counts, bar charts of the largest categories
* **Assess data quality**: for relevant fields, number of empty values, expected type, and check whether the values are what we expect. Consider if any missing values can be imputed.
* **Clean** if necessary/possible. Map string variables such as dates to integer representations if necessary.
* **Establish the distribution** of key variables, since this will inform which modelling tools can be applied.
* **Correlations**: the more 'inspiration' part of the process - depending on context, trying to detect relationships that are meaningful for the problem at hand.

### Tools to explore correlations

* correlation matrix (with heatmap coloration possibly)
* line plots (for timeseries for instance)
* box plots
* scatter plots

Number of other techniques [here](https://en.wikipedia.org/wiki/Exploratory_data_analysis)

### Focus
It's quite easy to spend too much time and lose focus in the last step of the data exploration.
To avoid this, it's good to:

* State at the start of exploration what we are trying to discover
* Write down the result in report form while working (whether a blog or actual client report) - this helps keeping it reasonably focused.
