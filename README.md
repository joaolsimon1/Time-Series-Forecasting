# Time Series Analysis: Modeling Maximum Temperature in Porto Alegre (RS), Brazil

## 📌 Project Description
This repository contains a final project for a Time Series Analysis course, focusing on modeling daily maximum temperatures in Porto Alegre, Brazil using data from INMET (National Institute of Meteorology). The main objective was to develop SARIMA models to predict daily maximum temperatures and compare their performance with actual 2023 data.

## Contents
- **RMarkdown Code**: (`time_series_analysis.Rmd`) contains the complete analysis, from data import to SARIMA modeling and validation.
- **Data**:
  - CSV files with daily temperature data (2012-2023) collected from Porto Alegre's meteorological station (INMET).
- **Results**:
  - Model 1: ARIMA(1,0,3) - Best AIC but visually less accurate.
  - Model 2: SARIMA(3,0,0)(0,1,0)[365] - Incorporates annual seasonality and shows better graphical fit.

## Key Steps
1. **Descriptive Analysis**:
   - Time series visualization, ACF/PACF, and seasonal decomposition.
   - Dickey-Fuller test for stationarity.
2. **Modeling**:
   - Automatic model selection with `auto.arima()`.
   - Residual diagnostics (Ljung-Box test, histogram, ACF).
3. **Forecasting**:
   - Comparison of forecasts (Jan-Jul 2023) with actual data.
   - Evaluation via AIC and graphical analysis.

## Conclusions
- **Model 1 (ARIMA)**: Best AIC (lowest value) but underestimates seasonal variations.
- **Model 2 (SARIMA)**: Better captures annual seasonality, with well-behaved residuals and superior visual fit.
- **Recommendation**: Use **Model 2** for predictions due to its ability to incorporate seasonal patterns.

## Technologies Used
- **R** (with packages: `forecast`, `tseries`, `dplyr`, `highcharter`, `ggplot2`).
- **RMarkdown** for dynamic reporting.
