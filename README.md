# PyRates
## Orignal Study:

Thompson, Philip R. et al. (2019). A Statistical Model for Frequency of Coastal Flooding in Honolulu, Hawaii, During the 21st Century. 124(4). https://doi.org/10.1029/2018jc014741
#### Using: MATLAB 
#### Data: [University of Hawai‘i Sea Level Center Fast Delivery database](http://uhslc.soest.hawaii.edu:80/opendap/fast/hourly/h057.nc)


## Recreating: 
Tidal Level Analysis & Modelling for Honolulu, Hawaii (2000-2024) for disaster mitigation & risk reduction strategies
[![DOI](https://zenodo.org/badge/810518524.svg)](https://zenodo.org/doi/10.5281/zenodo.11508504) 
#### Programming Language: Python (ver )
#### Software: Jupyter Notebook
#### Libraries used & version:


### Workflow:

| Steps     |  Description       | Links  |
| ------------- |:-------------:| -----:|
| Data Collection   | Collection of Data in CSV Format | [NOAA - Tides & Currents](https://tidesandcurrents.noaa.gov/waterlevels.html?id=1612340&units=standard&bdate=20140101&edate=20240527&timezone=GMT&datum=MLLW&interval=m&action=data) |
| Data Preprocessing| Using Pandas to check for missing values, imputation & transformation  |    |
| Statistical Analysis & Feature Extraction| Using Numpy|   |
|Data Visualisation| Using Matplotlib & pyleoclim |   |
| Modelling| Using Scikit Learn, StatsMods, TensoFlow for modelling |   |
| Model Evaluation| Evaluating Model using Performance Metrics   |   |
| Findings| Summarising Findings |    |



#### 1. Data Collection :
   a) Collected Data from NOAA - Tides & Currents: [Station: 1612340](https://tidesandcurrents.noaa.gov/waterlevels.html?id=1612340&units=standard&bdate=20140101&edate=20240527&timezone=GMT&datum=MLLW&interval=m&action=data)
   
   b) Format of Data file: CSV file.
   
   c) Data contains measurements for Sea Level Rise (attributes): 
   
MHW: Mean High Water, MSL: Mean Sea Level,  MTL: Mean Tide Level,  MLW: Mean Low Water, MLLW: Mean Low Low
      Water, MHHW: Mean High High Water

#### 3. Data Preprocessing:
a) Checking for missing values

b) Imputation

c) Transformation
   
#### 5. Statistical Analysis & Feature Extraction:

a) Calculating 
b) Splitting Dataset into training and testing set: 80/20
#### 6. Data Visualisation

a) Time Series Line Plot 

b) Scatter plot

c) Box Plot
#### 7. Modelling

 a) Time Series Forecasting
 
 b) Predicting using Regression
 
 c) Classification of tidal levels
   
#### 8. Model Evaluation
    
#### 9. Findings:
    
