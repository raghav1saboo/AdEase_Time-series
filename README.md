# AdEase_Time-series

## AdEase Wikipedia Page View Forecasting

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/raghav1saboo/AdEase_Time-series/blob/main/AdEase_Time_Series_Forecasting.ipynb)

## Overview

This repository contains a Jupyter Notebook focused on understanding and forecasting the per-page view counts for various Wikipedia pages over a period of 550 days. The goal is to predict future page views to help AdEase optimize ad placement for their clients across different languages and regions.

AdEase is an ads and marketing company that aims to maximize ad clicks at minimum cost. This project contributes to their "Decipher" AI module by analyzing and predicting user engagement on Wikipedia pages.

## Problem Statement

The task is to analyze the time series data of Wikipedia page views and forecast future views. This will enable AdEase to strategically place advertisements for their clients, considering the expected traffic on different language-specific pages.

## Dataset

The project utilizes two CSV files:

* **`train_1.csv`**: Contains daily view counts for approximately 145k Wikipedia articles. Each row represents an article, and each column represents a specific date. The page name in this file follows the format: `SPECIFIC NAME _ LANGUAGE.wikipedia.org _ ACCESS TYPE _ ACCESS ORIGIN`.

* **`Exog_Campaign_eng.csv`**: Indicates whether a campaign or significant event occurred on a specific date that might have influenced page views for English Wikipedia pages (1 for campaign day, 0 otherwise). This serves as an exogenous variable. The download link for the dataset is: [https://drive.google.com/drive/folders/1mdgQscjqnCtdg7LGItomyK0abN6lcHBb](https://drive.google.com/drive/folders/1mdgQscjqnCtdg7LGItomyK0abN6lcHBb)

## Data Dictionary (from `train_1.csv` Page Name)

The `page` column in `train_1.csv` contains information structured as follows:

`SPECIFIC NAME _ LANGUAGE.wikipedia.org _ ACCESS TYPE _ ACCESS ORIGIN`

* **SPECIFIC NAME**: The title of the Wikipedia page.
* **LANGUAGE**: The language of the Wikipedia page (e.g., en, ja, de).
* **ACCESS TYPE**: The type of access (e.g., desktop, mobile web).
* **ACCESS ORIGIN**: The origin of the request (e.g., all-access, spider).

## Concepts Tested

The Jupyter Notebook implements the following concepts for time series analysis and forecasting:

* **Exploratory Data Analysis (EDA):** To understand the trends, seasonality, and patterns in the Wikipedia page view data.
* **Time Series Forecasting:**
    * **ARIMA:** Autoregressive Integrated Moving Average model.
    * **SARIMAX:** Seasonal Autoregressive Integrated Moving Average with Exogenous Regressors model (utilizing the campaign data for English pages).
    * **Prophet:** A forecasting procedure implemented in Python and R, developed by Facebook.

## Getting Started

1.  Clone this repository to your local machine:
    ```bash
    git clone [https://github.com/raghav1saboo/AdEase_Time-series.git](https://github.com/raghav1saboo/AdEase_Time-series.git)
    ```
2.  Navigate to the repository directory:
    ```bash
    cd AdEase_Time-series
    ```
3.  Download the dataset from the provided Google Drive link.
4.  Open and run the Jupyter Notebook `AdEase_Time_Series_Forecasting.ipynb`.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request.

## License

[Optional: Add a license if you have one, e.g., MIT License]
