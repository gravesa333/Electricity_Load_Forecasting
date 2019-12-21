# Time Series Project

For this project, three years of hourly electricity load data was scraped from the UC Berkeley open data source and used to forecast a month of electricity use for over 70 buildings on the UC Berkeley campus.

The range of collected electricity data was January 2016 through November 2019. Missing data was imputed, then the entire data set was summed into daily observations and split into a training set from January 2016 through October 2019 and a test set for November 2019. 

A baseline SARIMA model was used to forecast the electricity load for a single building for November 2019. ACF and PACF plots were used in addition to a GridSearch to find the ideal parameters for the SARIMA model. The model was validated through both train-test split validation and walk forward validation.  Then, the model was applied to the rest of the buildings.

The mean absolute percent error was calculated for all buildings' forecasts, and then a new model was created that included exogenous variables (specifically for holidays, i.e. whether a day was a holiday or not). Mean absolute percent errors were re-calculated and compared to the first models' MAPE's.  Finally, the best model was selected for each building.

All relevant information was exported to Tableau to display the forecasts in a dashboard.


### Jupyter Notebook Organization/Project Process

1. Scrape data from UC Berkeley open data source
	- Web_Scraping.ipynb
2. Impute missing weather data
	- Meter_Reading_Imputing.ipynb
	- Meter_Reading_Imputing_R1.ipynb
3. Preliminary Time Series Modeling
	- Time_Series_Modeling.ipynb
4. SARIMA baseline model with walk forward validation
	- New_SARIMA_Modeling_Validation.ipynb
5. SARIMA model applied to rest of buildings
	- New_SARIMA_More_Buildings_Validation.ipynb
6. Prepare prediction and MAPE data to be exported and used in Tableau dashboard
	- New_SARIMA_Presentation_Prep.ipynb
	