# Forecast Application with R-shiny
## <a href="https://mlombera.shinyapps.io/forecast_r-shiny/" target="_blank">Launch the Shiny app!</a>

## Summary
This shiny app allows users to forecast monthly demand by applying various time series models and comparing the performance of each model. There are four main functions of this application including:
- Uploading raw demand data in a csv format and filtering data
- Single SKU forecasts and visualization
- Batch SKU forecasts
- Statistical analysis/visualization

## Packages Utilized
- shiny
- zoo
- xts
- ggplot2
- devtools
- forecast
- data.table
- DT
- dygraphs
- dplyr
- lubridate
- stats
- tsbox
- tidyr
- padr
- shinythemes
- rio
- magrittr
- shinyjs
- rsconnect

## Features
- Users can filter data based on region, country, product, and SKU number. Users can also filter time series data that doesn't have the specified number of minimum observations or too many recent zero observations. The time series data can also be aggregated. 
- Users have the option to specify the parameters of the forecast such as how many months ahead to forecast, which models to apply, the size of the confidence interval, and how to split the time series data into training and test data sets. 
- Aside from individually forecasting time series data for individual SKUs, users have the option to batch forecast for multiple SKUs at once. This allows multiple forecasts to be generated quickly despite possibly applying all 12 models on multiple SKUs. Just like the individual forecasts, users can specify certain parameters of the forecast. 
- There is also the option to visualize the time series data for individual SKUs such as seasonality plots, ACF plots, and decomposed plots. 

## File Format
There is currently no file format validation built in. Files should have format as per the table below. A data set example is provided <a href=" " target="_blank">here</a>. 
  
|```Date```| ```SKU #```| ```Product```| ```Country```| ```Region```| ```Demand```|
|:---------------|:---------------|:---------------|:--------------|:---------------|:------------------|
|```dd/mm/yyyy```| ```SKU # 1```	|	```Product A```|```Country A```| ```Region A```	|	```Demand Value```|
|```dd/mm/yyyy```| ```SKU # 2```	|	```Product B```|```Country B```| ```Region B```	|	```Demand Value```|
|```dd/mm/yyyy```| ```SKU # 3```	|	```Product C```|```Country C```| ```Region C```	|	```Demand Value```|

## Current Bugs