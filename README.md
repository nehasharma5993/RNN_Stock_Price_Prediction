# Project Name : Stock Price Prediction using RNN

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
  

## General Information
- The objective of this assignment is to try and predict the stock prices using historical data from four companies: IBM (IBM), Google (GOOGL), Amazon (AMZN), and Microsoft (MSFT) belonging to the same sector i.e.Technology.
- The dataset consists of four CSV files corresponding to four stocks: AMZN, GOOGL, IBM, and MSFT.
- There are more than 3000 records for each company spread across the years. The columns in all four files are identical, which are: Date, Open, Close, High, Low, Volume and Name. 
  

## Conclusions
- In this project, we developed and evaluated several recurrent neural network models (Simple RNN, LSTM, and GRU) to predict the closing prices of four major technology stocks: Amazon, Google, IBM, and Microsoft.
- Among the tested models, the advanced RNN architectures (LSTM and GRU) generally outperformed the Simple RNN, especially when using stacked layers and dropouts.
- Hyperparameter tuning (units, dropout, learning rate, batch size, and epochs) was crucial for optimizing model performance.
- Stacked LSTM/GRU layers with dropout helped prevent overfitting and improved generalization.
- We selected a window size of 63 days, which roughly corresponds to a financial quarter (about three months of trading days) and step size was set to 1, meaning the window moves forward by one day at a time.
- The best model (e.g., GRU with 128 units, 0.3 dropout, and 30 epochs) achieved an average MAE and RMSE that are acceptable for financial time series forecasting.
- Amazon: MAE = 794.23, RMSE = 813.65, R² = -0.27
- Google: MAE = 827.25, RMSE = 834.67, R² = 0.41
- IBM: MAE = 151.58, RMSE = 152.07, R² = -2.87
- Microsoft: MAE = 58.08, RMSE = 58.94, R² = 0.33
- The model performed best on Microsoft and Google, as indicated by their positive R² values but struggled with IBM, which had a negative R².
- The MAE and RMSE values are relatively high for Amazon and Google, likely due to their higher price ranges and volatility.
- The results highlight that while the RNN-based approach can capture some temporal patterns, further improvements are needed, especially for stocks with more complex or volatile price behavior


## Technologies Used
- numpy: 2.1.3
- pandas: 2.2.3
- seaborn: 0.13.2
- sklearn: 1.6.1
- tensorflow: 2.19.0
- tensorflow keras: 3.9.2


## Acknowledgements
- I would like to express gratitude to the UpGrad IITB Programme for providing me with the opportunity to implement Stock Price Prediction using RNN as part of our coursework. 
- This case study has enriched our understanding and practical application of data analysis and machine learning techniques, contributing significantly to our learning experience.


## Contact
Created by [@nehasharma5993] and [@niranjantitan76]


## License
This project is open source and available without restrictions.
