### Relationships between QQQ ETF Price and NASDAQ 100 Technology Stocks (Classification, Prediction)| Python

In the ever-evolving landscape of financial markets, understanding the intricate relationships between individual stocks and exchange-traded funds (ETFs) is crucial for informed decision-making. This machine learning (ML) project investigates the relationships between the stock prices  companies listed on the Nasdaq 100 index and the corresponding prices of the QQQ ETF.
### Method:
Sourced historical stock data from Alpaca
Data Preprocessing:
Cleaned and preprocessed the historical stock data. 
Normalized or scaled the data as required.
Feature Engineering:
Extracted relevant features for analysis.
Explored corelations
Model Building:
Implemented a Linear Regression model to establish a baseline understanding of relationships.
Applied Lasso Regression to identify key features and mitigate overfitting.
Utilized PCA to mitigate overfitting and tried another Linear Regression model.
Developed KNN classification models to identify stock group prices that drove index.
Implemented Adaboost for classification as final model.

### Results
The project sought to find a relationship between the top 10 ten and bottom 10 technology company stocks in the NASDAQ index and their relationship to the price of the QQQ ETF.
Models built were Least squares regression models (for baseline), which performed very well on the trainging data but overfit the test data. Weights that determine the model features and how they act to determine the price of the QQQ were showcased. However the least squares regression model was not a very good one due to over fitting. A Lasso regression model was also built and it reduced overfitting but the low R-squared values in the train and test data, indicated a weak regression model.
PCA was used to transform the data and a new regression model was built. The low R-squared value indicated that the model also did not perform well on the data, however it seemed to predict the rise and fall of the prices in the test data pretty well. This could perhaps be due to the fact that r-sqaured values on regression models built on financial data are typically low.
The KNN classifier had high accuracy and precision scores. It performed well on the test data and indicated strong potential in classifying a high or a low for a new intance time . It could also be used to indicate stocks that will potentially rise with the QQQ ETF.
The Adaboost Classifier worked best. It had a high accuracy and Precision. It will indicate/classify which Nasdaq stock price will rice or fall with the QQQ. Other potential uses of the classifer in relation to the relationship of the stock prices can be applied. 
As can be seen from graph on the test set,the Adaboost classifier model fits perfectly on the test set when the predicted vs actual labels are ploted on the time series.
