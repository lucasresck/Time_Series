# time-series-2

Assignment codes for [Time Series](https://emap.fgv.br/sites/emap.fgv.br/files/u77/series_temporais.pdf) (2020, FGV).

In this repository, we study several topics included in Time Series subject,
such as ARIMA models, trend and seasonality. Each homework has a pratical study and
some theorical questions. Alternative projects to the beggining of the course (Covid-19 deaths analysis and homework 1)
can be found in [this repository](https://github.com/lucasresck/time-series).

The homeworks and assigments are coded in R language and the presentations and
texts are in Portuguese. If requested, the authors can translate it. 

## R programming 

R is the classic programming language for statistics. It has some limitations
when compared to other languages, but some packages make it more worthy, as: 

1. `ggplot`: best tool for plotting in R
2. `tseries` and `zoo`: good for dealing more easily with time series. 
3. `forecast`: the best when we speak about estimation and predictions of the models. 

## Homework 1 

A pratical study of Car's Sales in Norway. In this study we practice the
following modelling: 

- Decomposition in [Seasonal, Trend and Remainder](https://otexts.com/fpp2/stl.html) of a Time Series;
- Polynomial regression for trend and seasonality;
- Holt-Winters and Exponential Smoothing.

After each modelling, we compared the models using the [Mean Absolute
Percentage
Error](https://en.wikipedia.org/wiki/Mean_absolute_percentage_error). 

Above you can see the moving average decomposition and the final comparison
among the models. 

<img src="images/moving_average_decomposition_hw1.png" alt="drawing" width="600"/>

<img src="images/comparison_model_hw1.png" alt="drawing" width="600"/>

## Homework 2

Identification of ARMA models, considering the Autocorrelation and Partial
Autocorrelation of the series. 

By looking the image, the behaviour of the graphic can identify, initially, a
model.

<img src="images/acf_pacf_hw2.png" alt="drawing" width="600"/>

## Homework 3

We have some theorical exercises about differenciation and stationarity of
ARIMA process. Also we construct by simulation the distribution of the
statistic of [Adjusted Dickey-Fuller (ADF)
Test](https://en.wikipedia.org/wiki/Augmented_Dickey%E2%80%93Fuller_test). In
the end we identify an ARIMA model for the IPCA (inflation) series. We
considered a variance stabilizer. So as to identify the model, we use the ACF
and PACF graphics combined by the [Information
Criterion](https://en.wikipedia.org/wiki/Model_selection#Criteria), as AIC,
BIC and AICc.

<img src="images/ipca_monthly_hw3.png" alt="drawing" width="600"/>

For each considered model, we studied the residuals of the estimated model. 

<img src="images/residual_analysis_hw3.png" alt="drawing" width="600"/>

## Homework 4 

We used the method Box-Jenkins in order to understand a time series as an
ARIMA model. We can summarize it as: 

1. Box-Cox transformation to stabilize the variance. 
2. Identify the ARIMA(p,d,q) model: 
   1. Check the stationarity of the series with ADF test and differentiate  if
   necessary (d times)
   2. Visualize the ACF and PACF of the data. 
   3. Compare AIC, BIC and AICc information and select p and q. 
3. Estimation of the parameters of the model through maximum likelihood. 
4. Diagnose the residuals (remainder of the fitting): 
   1. Visualize the residuals.
   2. Plot histogram, autocorrelation and partial autocorrelation. 
   3. Ljung-Box's test for de-correlation and Jarque-Bera's test for kurtosis
      and skewness' normality. 

## Homework 5 

More exercises about transformation of a time series. We study the Box-Jenkins
method considering seasonality. In this case, it's important to use
Kruskal-Wallis test for seasonality and differentiate D times considering
this. The information criterion and ACF can be used as well. As example, we
used the expenses in coffees, restaurants and other in Australia. 

<img src="images/eating_hw5.png" alt="drawing" width="600"/>

## Assignments 

The assigments are application of this methods in more difficult series. It's
suggested to have a look in the pdfs available in the assigment's folder.
