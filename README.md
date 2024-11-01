
# PyRates
Title: # Forecasting Tidal Dynamics Across Hawaiian Islands: A Multivariate Time Series Analysis Using LSTM, Transformers, and Seasonal Models

## Orignal Study:

Thompson, Philip R. et al. (2019). A Statistical Model for Frequency of Coastal Flooding in Honolulu, Hawaii, During the 21st Century. 124(4). https://doi.org/10.1029/2018jc014741
#### Using: MATLAB 
#### Data: [University of Hawai‘i Sea Level Center Fast Delivery database](http://uhslc.soest.hawaii.edu:80/opendap/fast/hourly/h057.nc)


## Recreating: 
Tidal Level Analysis & Modelling for Honolulu, Hawaii (2000-2024) for disaster mitigation & risk reduction strategies
[![DOI](https://zenodo.org/badge/810518524.svg)](https://zenodo.org/doi/10.5281/zenodo.11508504) 
#### Programming Language: Python (python3.12)
#### Software: Jupyter Notebook
#### Libraries used & version:


## Project Overview

This project explores the application of advanced deep learning models, such as LSTM networks and Transformer models, along with seasonal methods, to forecast tidal levels across various Hawaiian islands. The goal is to create a robust predictive model to understand and forecast tidal features like the highest tide, mean sea level (MSL), and lowest tide.

Understanding these patterns is crucial for:
- Coastal management
- Climate impact assessments
- Environmental monitoring

The forecasted results aim to support decision-making for coastal infrastructure planning, flood risk management, and studying the effects of climate change on sea levels.

---

## Data Source

Data is sourced from NOAA's [Tides & Currents](https://tidesandcurrents.noaa.gov/) and includes records from four Hawaiian stations:
- **Hilo** (Station ID: 1617760)
- **Honolulu** (Station ID: 1612340)
- **Kawaihae** (Station ID: 1617433)
- **Nawiliwili** (Station ID: 1611400)

---

## Workflow

| Steps                                | Description                                                                                     | Libraries/Tools                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------|
| **Data Collection**                  | Collection of historical tidal data in CSV format                                              | NOAA - Tides & Currents                           |
| **Data Preprocessing**               | Handling missing values, feature engineering, and scaling                                      | Pandas, SciPy                                     |
| **Statistical Analysis & Feature Extraction** | Seasonal decomposition and trend analysis                               | Statsmodels, SciPy                                |
| **Data Visualization**               | Graphical representation of tidal patterns and correlations                                    | Matplotlib, Seaborn                               |
| **Modeling**                         | Applying LSTM, Transformer models, and hybrid seasonal models                                  | TensorFlow, Statsmodels, SciPy                    |
| **Model Evaluation**                 | Assessing model performance using RMSE and MAE                                                 | Sklearn                                           |
| **Forecasting**                      | Generating 10-year forecasts and identifying seasonal patterns                                 | Fourier + SARIMA Hybrid Model                     |
| **Findings**                         | Summarizing results and implications                                                           | Textual analysis, Data visualization              |

---

## Modeling Techniques

### Hybrid ARIMA + LSTM Model
- **ARIMA**: Utilized to capture linear trends and seasonal components in the time series data.
- **LSTM**: Applied to model non-linear, complex patterns, particularly in the residuals from ARIMA, which allows for accurate short- and long-term predictions.

### Hybrid Fourier + SARIMA Model
- **Fourier Series**: Employed to capture the cyclical, seasonal patterns in tidal data.
- **SARIMA**: Used to refine predictions by addressing residual patterns and irregular short-term fluctuations not captured by Fourier components.


---

## Residual Summary Tables

### Model Performance Summary

| Station     | Model               | RMSE   | MAE    |
|-------------|----------------------|--------|--------|
| Hilo        | ARIMA + LSTM Hybrid  | 0.33 ft | 0.26 ft |
| Honolulu    | ARIMA + LSTM Hybrid  | 0.31 ft | 0.25 ft |
| Kawaihae    | ARIMA + LSTM Hybrid  | 0.38 ft | 0.32 ft |
| Nawiliwili  | ARIMA + LSTM Hybrid  | 0.30 ft | 0.24 ft |

### Forecast Highlights

| Station     | Peak Tide Period   | Highest Predicted Tide Level |
|-------------|--------------------|------------------------------|
| Hilo        | December           | 3.72 ft (2029)              |
| Honolulu    | December           | 3.06 ft (2029)              |
| Kawaihae    | August             | 3.51 ft (2030)              |
| Nawiliwili  | August & December  | 2.98 ft (2030)              |

