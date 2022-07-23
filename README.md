# Cowboy Cigarettes Case Study

You're working in the US federal government as a data scientist in the Health and Environment department. You've been tasked with determining whether sales for the oldest and most powerful producers of cigarettes in the country are increasing or declining.

Cowboy Cigarettes (TM, est. 1890) is the US's longest-running cigarette manufacturer. Like many cigarette companies, however, they haven't always been that public about their sales and marketing data. The available post-war historical data runs for only 11 years after they resumed production in 1949; stopping in 1960 before resuming again in 1970. Your job is to use the 1949-1960 data to predict whether the manufacturer's cigarette sales actually increased, decreased, or stayed the same. You need to make a probable reconstruction of the sales record of the manufacturer - predicting the future, from the perspective of the past - to contribute to a full report on US public health in relation to major cigarette companies.

The results of your analysis will be used as part of a major report relating public health and local economics, and will be combined with other studies executed by your colleagues to provide important government advice.

### Project Stucture

We begin by doing some cleaning of the CowboyCigsData.csv data set, which, when cleaned, consists of only a monthly index and a column of cigarette sales.

We then visually explore the data with a basic plot and with a seasonal decomposition plot to see that there is trend, seasonality, and a non constant variance. 

We then iterate over a range of p, d, and q values to find an ARIMA model with the least error, which happened to be a (2, 1, 1) ARIMA model. With it, we can make our forecast.

### Packages

The basic packages used are

- pandas
- numpy
- matplotlib

For the time series and modeling sections, we used various modules from the statsmodels library. We also used the mean squared error metric from scikit-learn. Instructions for installing both packages can be found at the following websites:

statsmodels: https://www.statsmodels.org/stable/install.html

scikit-learn: https://scikit-learn.org/stable/install.html