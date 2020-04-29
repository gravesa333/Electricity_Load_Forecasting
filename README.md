# Time Series Project

For this project, three years of hourly electricity load data was scraped from the UC Berkeley open data source and used to forecast a month of electricity use for over 70 buildings on the UC Berkeley campus.

The electricity data was collected for days from January 2016 through November 2019. The dataset was split into training and test sets, missing data was imputed, then the hourly data was summed into daily observations.

A baseline SARIMA model was used to forecast the electricity load for a single building for November 2019. ACF and PACF plots were used in addition to a GridSearch to find the ideal parameters for the SARIMA model. The model was validated through both train-test split validation and walk forward validation.  Then, the model was applied to the rest of the buildings.

The mean absolute percent error was calculated for all buildings' forecasts, and then a new model was created that included exogenous variables (specifically for holidays, i.e. whether a day was a holiday or not). Mean absolute percent errors were re-calculated and compared to the first models' MAPE's.  Finally, the best model was selected for each building.

All relevant information was exported to Tableau to display the forecasts in a dashboard (see "Load_Forecasting_Dashboard.twb" in Presentation folder).

See blog post published on Towards Data Science for more details (along with the notebooks listed in the outline below): [Time Series Forecasting with a SARIMA Model] (https://towardsdatascience.com/time-series-forecasting-with-a-sarima-model-db051b7ae459)


### Jupyter Notebook Organization/Project Process

1. Scrape data from UC Berkeley open data source
	- Web_Scraping.ipynb
2. Impute missing data
	- Meter_Reading_Imputing.ipynb
	- Meter_Reading_Imputing_R1.ipynb
3. SARIMA baseline model with walk forward validation
	- New_SARIMA_Modeling_Validation.ipynb
4. SARIMA model applied to rest of buildings
	- New_SARIMA_More_Buildings_Validation.ipynb
5. Prepare prediction and MAPE data to be exported and used in Tableau dashboard
	- New_SARIMA_Presentation_Prep.ipynb
	