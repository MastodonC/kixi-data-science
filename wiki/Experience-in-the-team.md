We have a number of data science projects behind us.  This page should inventory which techniques we used, which projects used it, and what kind of situations it's suitable for.

This should help us retrieve past experience when approaching a new project that looks like it might need a similar approach.

### Modelling

#### AutoRegressive Integrated Moving Averages
**Definition**:
"In statistics and econometrics, and in particular in time series analysis, an autoregressive integrated moving average (ARIMA) model is a generalization of an autoregressive moving average (ARMA) model. Both of these models are fitted to time series data either to better understand the data or to predict future points in the series (forecasting). ARIMA models are applied in some cases where data show evidence of non-stationarity, where an initial differencing step (corresponding to the "integrated" part of the model) can be applied one or more times to eliminate the non-stationarity."
[Wikipedia definition](https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average)

**When to use**:
When we want to project a timeseries forward based on just the information it contains by itself (value - time).  This is a bit of a quick-fix method if time is short or no obvious correlations have been found which could be used to do a sensible regression.

**Projects this has been used in**:

* Fast-SBRI: predict patients coming into the different wards of the hospital
https://github.com/MastodonC/kixi.fast-SBRI
* Employment for B&NES: predict the next 20 years of employment in the B&NES area
https://github.com/MastodonC/employment-exploration

**Current toolset**: we have used the R implementation.  There's a default _arima_ function in R, and the forecast package adds a _forecast_ function which seems to be slightly more robust than the default _predict_ function.

#### Markov Chain Monte Carlo
...


#### Latent Dirichlet Allocation
...


### Visualization/type of diagram
Which is the most effective, non-trivial way to represent a certain type of data?  What have you used in the past?
