# Bitcoin Price Time Series Analysis

This project performs a time series analysis of Bitcoin's historical prices using Python. It focuses on visualizing price fluctuations between April 2013 and July 2017, examining key price indicators such as Open, High, Low, Close, Volume, and Market Cap. The project also includes interactive candlestick charts to provide insights into daily price movements.

## Table of Contents
- [Project Structure](#project-structure)
- [Data](#data)
- [Visualizations](#visualizations)
- [Libraries Used](#libraries-used)
- [How to Run](#how-to-run)
- [Conclusion](#conclusion)

## Project Structure

- **Data Loading and Exploration**:  
   - Data is loaded using `pandas` and explored to understand key metrics.
   - Key columns in the dataset:
     - `Date`: The date of the trading day.
     - `Open`, `High`, `Low`, `Close`: Prices at different stages of the day.
     - `Volume`: The trading volume.
     - `Market Cap`: Market capitalization on the given day.
   - Statistical summaries help in understanding central tendencies and variations in Bitcoin prices.

- **Data Cleaning**:
   - The `Date` column is converted to `datetime64` format.
   - The dataset is cleaned from null values and duplicates.

- **Data Sorting**:  
   - Data is chronologically sorted for accurate time series visualization.

- **Data Visualization**:
   - **Line Plots**: Created using `matplotlib` and `seaborn` for key price indicators over time.
   - **Candlestick Chart**: Created using Plotly’s `go.Candlestick` function, this provides a detailed view of the price behavior over a sample of 50 days.

## Data

The dataset used contains daily Bitcoin price data from April 2013 to July 2017. Key columns include:
- **Date**: Trading date.
- **Open**: Opening price of Bitcoin on the given day.
- **High**: Highest price reached on the day.
- **Low**: Lowest price reached on the day.
- **Close**: Closing price of Bitcoin on that day.
- **Volume**: Amount of Bitcoin traded during the day.
- **Market Cap**: Total value of Bitcoin in the market on that day.

## Visualizations

- **Line Charts**: Visualize the `Open`, `High`, `Low`, and `Close` prices over the entire dataset.
  
  Example:
  ```python
  plt.figure(figsize=(20, 12))
  for index, col in enumerate(['Open', 'High', 'Low', 'Close'], 1):
      plt.subplot(2, 2, index)
      plt.plot(data['Date'], data[col])
      plt.title(col)

