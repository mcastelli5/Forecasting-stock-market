# Forecasting-stock-market

The purpose of this project is to focus on the technical aspects of the stock market, in an attempt to develop a trading strategy that increases potential future gains. The financial instrument analyzed is the SPY ETF (sourced from Yahoo! and Google), which represents the stocks from the S&P 500.

Throughout the forecasting process, two different machine learning algorithms were utilized and benchmarked against each other to determine the optimal strategy: Support Vector Modeling (more specifically, Support Vector Regression) and Dynamic Time Warping (DTW). In addition to the ML models, basic intraday and overnight strategies were used as a baseline to analyze how effective the ML models were in beating a simple trading strategy. Each strategy was assessed by a few statistical/financial metrics, such as, overall trade quantity, gains (wins), losses, averages, standard deviation (volitatilty), and the Sharpe Ratio.

## Support Vector Regression

Support Vector Machine (SVM) models are common amongst classification problems, however, Support Vector Regression (SVR) is a highly flexible and easy-to-implement supervised learning approach for regression analysis. The overall objective of SVR is to minimize the vector coefficients, unlike simple linear regression which focuses on minimizing the sum of squared errors. Therefore, the main benefit that SVR provides over simple linear regression models, is the ability to define the amount of error that is acceptable within the model, while independently maintaining its computational complexity. In addition, SVR provides an excellent generalization capability with high prediction accuracy.

Specific to the project, the SVR model was found to be less effective than the simple intraday and overnight trading strategies (for that specific time period). Even when the time period was extended and the model restraints were updated, the regression acted more as a contrarian indicator for buying/selling the SPY ETF.

## Dynamic Time Warping

The objective of Dynamic Time Warping (DTW) is to determine the optimal match between two temporal sequences (time series) by measuring pattern similarities. DTW is one of many algorithms that is used in time series analysis, and more specifically in an attempt to analyze the financial markets / financial data. This approach focuses more on the pattern of the data, which bypasses the exhaustive requirement of test and train data that other time series analysis algorithms need to produce similar features.

Specific to the project, DTW was found to be the most effective approach to forecasting the stock market (based on the SPY ETF and within the specific time period). DTW allowed for a more technical analysis of the SPY ETF stock price, by assessing the statistical trends (patterns). At the end of the jupyter notebook, I was able to confirm my algorithm was matching similar patterns, and used those to better forecast future stock market movements.

## Conclusion

Although consistently forecasting the stock market is a near impossible task, the excerise of applying two entirely different algorithms and comparing them to baseline approaches outlined a simple overview of how ML models can assist in everyday activites, such as trading. For this exact time period and fund, the techincal strategy (DTW) proved to be more accurate at forecasting buying opportunities to gain value in the market. This is just the beginning to understanding the markets, and there are a lot of other factors that are important to consider for more in-depth analysis such as: portfolio construction, risk mitigation, money management, etc...

## Language Used

- Python

## Libraries Used

- Pandas
- Numpy
- Pandas_datareader
- Matplotlib
- Sklearn.svm
- Scipy.spatial.distance (for DTW Euclidean distance)
- Fastdtw
