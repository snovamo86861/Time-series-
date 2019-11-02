# Time Series

A useful abstraction for selecting forecasting methods is to break a time series down into systematic and unsystematic components.

* Systematic: Components of the time series that have consistency or recurrence and can be described and modeled.

* Non-Systematic: Components of the time series that cannot be directly modeled.

A given time series is thought to consist of three systematic components including level, trend, seasonality, and one non-systematic component called noise.

These components are defined as follows:

* Level: The average value in the series.
* Trend: The increasing or decreasing value in the series.
* Seasonality: The repeating short-term cycle in the series.
* Noise: The random variation in the series.

# Stationary

Stationarity is an  important aspect of time series as we can assume that future statistical properties are the same or proportional to current statistical properties.

if the series we want to predict is stationary, and if it is not,finding ways to transform it such that it is stationary.

* Mean of a time series $x_t$ is $E(x_t)=\mu(t)$

* Variance of a time series $x_t$ is $\sigma^2(t)=E[(x_t - \mu(t))^2]$

* A time series is stationary in the mean if $\mu(t)=\mu$, i.e.mean is constant with time

* A time series is stationary in the variance if $\sigma^2(t)=\sigma^2$, i.e. variance is constant with time

![Correlation](https://github.com/Auquan/Tutorials/raw/0565b9f61a2c2361bcfc25fc6442ad66c2aefb43/download.png)

# What Is Autocorrelation?

Autocorrelation is a type of serial dependence. Specifically, autocorrelation is when a time series is linearly related to a lagged version of itself. By contrast, correlation is simply when two independent variables are linearly related.

The most compelling aspect of autocorrelation analysis is how it can help us uncover hidden patterns in our data and help us select the correct forecasting methods. Specifically, we can use it to help identify seasonality and trend in our time series data. Additionally, analyzing the autocorrelation function (ACF) and partial autocorrelation function (PACF) in conjunction is necessary for selecting the appropriate ARIMA model for your time series prediction.

![Auto](https://miro.medium.com/max/2298/1*1SnyrVnYQ747DkltaH6nkQ.png)

Above is an example of an autocorrelation plot. Looking closely, you realize that the first value and the 24th value have a high autocorrelation.

# Stationarity

 A time series is said to be stationary if its statistical properties do not change over time. In other words, it has constant mean and variance, and covariance is independent of time.

![Auto](https://miro.medium.com/max/2904/1*tCCq8QoJGYTmrJZiYafLlw.png)

Looking again at the same plot, we see that the process above is stationary. The mean and variance do not vary over time.

Often, stock prices are not a stationary process, since we might see a growing trend, or its volatility might increase over time (meaning that variance is changing).



# Modelling time series

There are many ways to model a time series in order to make predictions. Here, I will present:

* Moving average: Can be used to identify interesting trends in the data. We can define a window to apply the moving average model to smooth the time series, and highlight different trends.

* Exponential smoothing: Uses a similar logic to moving average, but this time, a different decreasing weight is assigned to each observations. In other words, less importance is given to observations as we move further from the present.

* ARIMA: It is the combination of simpler models to make a complex model that can model time series exhibiting non-stationary properties and seasonality.

