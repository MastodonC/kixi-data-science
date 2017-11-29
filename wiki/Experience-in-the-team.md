We have a number of data science projects behind us.  This page should inventory which techniques we used, which projects used it, and what kind of situations it's suitable for.

This should help us retrieve past experience when approaching a new project that looks like it might need a similar approach.

### Modelling

#### AutoRegressive Integrated Moving Averages

**Definition**:
"In statistics and econometrics, and in particular in time series analysis, an autoregressive integrated moving average (ARIMA) model is a generalization of an autoregressive moving average (ARMA) model. Both of these models are fitted to time series data either to better understand the data or to predict future points in the series (forecasting). ARIMA models are applied in some cases where data show evidence of non-stationarity, where an initial differencing step (corresponding to the "integrated" part of the model) can be applied one or more times to eliminate the non-stationarity."
[Wikipedia definition](https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average)

**When to use**:
When we want to project a timeseries forward based on just the information it contains by itself (value - time).  This is a bit of a quick-fix method if time is short or no obvious correlations have been found which could be used to do a sensible regression. It's good for incorporating seasonal patterns. 

**Relevant Projects**:

* Fast-SBRI: predict patients coming into the different wards of the hospital
https://github.com/MastodonC/kixi.fast-SBRI
* Employment for B&NES: predict the next 20 years of employment in the B&NES area
https://github.com/MastodonC/employment-exploration

**Current toolset/libraries**:
We have used the R implementation.  There's a default _arima_ function in R, and the forecast package adds a _forecast_ function which seems to be slightly more robust than the default _predict_ function.

**Who is expert in it**: Elise, Seb

#### Markov Chain Monte Carlo
**Definition**:

**When to use**:

**Projects this has been used in**:

**Current toolset/libraries**:

**Who is expert in it**: Henry, Seb

#### Latent Dirichlet Allocation
**Definition**:

**When to use**: When you need to find the topics of a corpus and predict the topics of a particular bit of text.

**Projects this has been used in**: Arup reports analysis; Defra animal disease detection; Building reports for IUK; ONS P5

**Current toolset/libraries**: https://github.com/MastodonC/kixi.mallet

**Who is expert in it**: Henry, Jase, Fran, Bruce. Mike/Seb starting to get involved via ONS work. 

#### Clustering 
**Definition**:

**When to use**:

**Projects this has been used in**: Arup reports analysis; C40; Policy Lab employment analysis

**Current toolset/libraries**:

**Who is expert in it** Seb, Fran

#### Cohort Component Models
**Definition**:
Cohort Component models are used for population estimates and projections.
"The concepts of population estimates and population projections often are confused even though the distinction between the two is relatively simple and straightforward. Both concepts involve the generation of a number that is intended to indicate the size of the population of a given geographic area at a specific point in time. Both techniques make use of the basic demographic equation:
```
P2 = P1 + B - D + I - O
```
which indicates that the population at any given point in time (P2) is a function of the population at a previous point in time (P1) plus the amount of natural increase (births minus deaths) and the net migration (in-migration minus out-migration) during the interim.
...
Population change involves three separate components: births, deaths, and migration. Component models consider the separate effects of each of these factor and require more comprehensive and detailed data than usually are available to local planners. Models that use the net effects of the three components are called noncomponent models."
(<http://www-personal.umich.edu/~steiss/page55.html>)

In short, the population is projected by:

* aging all age groups by 1 year
* adding births and incoming migration based on past births and migration (linear regression or other)
* subtracting deaths and outgoing  migration based on past deaths and migration

**When to use**:
This was used in the context of the GLA - transcribing one of their existing models into code.  We have discontinued work on demography models, but they may still be a side factor in future models.

**Projects this has been used in**:
GLA population models: https://github.com/MastodonC/witan.models.demography

**Current toolset/libraries**:
Straightforward clojure.

**Who is expert in it**: Sunny, Seb

### Visualization/type of diagram

Which is the most effective, non-trivial way to represent a certain type of data?  What have you used in the past?

**Sankey diagrams** are a big help in representing complex flows of people or things through a set of stages or categories, for example animals from symptom to diagnosis, students changing schools in SEND modela. 
