# Trinity-Prediction-Trideque-Prophet-Bitcoin
This is a Python script that predicts the price of Bitcoin for the next day, week, and month using the historical Bitcoin price data from Alpha Vantage. The script uses the Prophet library, a forecasting tool developed by Facebook, to make predictions.

Here's a breakdown of the code:

Dependencies are installed using !pip install.

numpy: A library for numerical computing in Python.
requests: A library for making HTTP requests.
scikit-learn: A library for machine learning in Python.
prophet: A library for time-series forecasting.
The necessary libraries are imported.

The get_historical_data function fetches historical Bitcoin price data from Alpha Vantage API. It returns a dictionary with timestamps as keys and corresponding closing prices (in USD) as values.

The historical_data_to_dataframe function converts the historical data dictionary to a pandas DataFrame, which is required by the Prophet library.

The make_prediction function takes a trained Prophet model, the latest DataFrame, and the number of days into the future to predict. It creates a future DataFrame using the make_future_dataframe method and then makes predictions using the predict method. Finally, it returns the predicted values.

The main function does the following:

Calls get_historical_data to fetch the historical Bitcoin price data.
Converts the historical data to a pandas DataFrame using historical_data_to_dataframe.
Trains a Prophet model on the DataFrame.
Calls make_prediction three times to get predictions for tomorrow, next week, and next month.
Prints the predictions.
The if __name__ == '__main__': line ensures that the main function is only called when the script is run directly and not when imported as a module.
