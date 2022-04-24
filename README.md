# SC1015 Mini Project - Twitch
Our team's objective is to make use of the the Twitch's API to help out small or upcoming streamers on how to be opular on twitch. In our project, we will be extracting data from the most popular streamers and find out what factors propels these streamers to become a twitch superstar.
![image](https://user-images.githubusercontent.com/102810962/164954067-f02bca75-5dbb-4495-b3af-2bce64ef6d70.png)
## Tech Stack
- Data retrieval: Twitch API Platform, XMLHttprequest from twitchtracker.com
- Data wrangling: Python
- Data visualisation: Tableau
- Presentation: PowerPoint, Windows movie maker
- 
## Algorithms/Libraries
- Pandas, seaborn
- Naive-bayes
- Linear regression

## FSP5_Team07 Folder
### Slides: FSP5_Team07 Slides
The slides provide a quick summary of our project. It covers the overall aim of our project, data extraction and preparation from the APIs, our analysis using regression and time-series forecasting, and the conclusions we draw from our work.

### Jupyter Notebook #1: Data Extraction & Exploratory Analysis
The code in this notebook is used to extract data from the various files to form our datasets and visualise our datasets to gain insights. For data extraction, all bus stops and MRT stations are being grouped by subzones. The demographics data and public transportation traffic data are then being aggregated by subzones, and datasets are being created to aid in exploratory analysis, time series forecasting and regression. For exploratory analysis, the spreads of all the variables in the datasets the correlation among them are being inspected. Tableau (included in our submission) is also being employed to gain further insights on the data.

### Jupyter Notebook #2: Machine Learning - Time Series Forecast (AR, ARIMA)
The code in this notebook is used to forecast demographics data for 2025 based on our dataset containing demographics data from 2011-2020.
Autoregression and ARIMA are being assessed for their suitabilility on our dataset from Notebook #1. For autoregression, the existence of autocorrelation using a lag plot is being determined and stationarity is checked for by using a time-series plot and the Augmented Dickey-Fuller test. The ADF score is then used to decide whether to apply a transformation. Autoregression on the transformed data is then determined to have a higher R-squared. ARIMA is the being applied, but it was deemed to be a weaker model than autoregression even with optimal hyperparameters. Autoregression is then being used to forecast the demographics data for 2025.

### Jupyter Notebook #3: Machine Learning - Regression (Linear, Random Forest)
The code in this notebook is used to predict public transportation demand by subzone in 2025 using datasets from Notebooks #1 and #2. Univariate regression is bering performed on each of the eight variables in the dataset and 6 of the variables with the highest explained variance and lowest mean squared error are being chosen to be used in the regression model. The suitability of multivariate linear regression, decision tree regression and random forest regression is being assessed for the dataset. Having have the highest R-squared, random forest regression is being deemed the most appropriate regression model. The random forest regression model is then applied onto the forecasted demographics data from Notebook #2 to predict ransportation traffic in 2025. The 20 subzones with the heaviest public transportation traffic in 2025 are subsequently being predicted.
