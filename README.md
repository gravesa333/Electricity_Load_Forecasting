# Time Series Project

**To-Do List**

- Run remaining models
	- Fix SARIMA parameters for models that didn't run
		- 603, 604, 618
	- Fine-Tune models that have error > 15%
		- 568 (11.975%)
		- 571 (11.020%)
		- 599 (15.622%)
		- 601 (18.331%)
		- 605 (11.248%)
		- 610 (21.002%)
		- 621 (10.592%)
		- 634 (18.252%)
		- 636 (15.895%)
- Create powerpoint slides
- Create Tableau dashboard

___

### ASHRAE Project

- Temperatures are in C or F based on location
- Times are not local (temp peaks occur at different hours depending on the site
- 3750 outliers for meter_reading due to 2 buildings (**1099, 778**)
- 29 outliers for square_feet
- 5 outliers for floor_count
- Wind direction duplicates (0 and 360 are the same)
- Site 0 has zero or small readings in first 5 months in 2016
- Potential meter reading failures (replace with mean values like with weather?)
- missing floor count
	- 
- missing year built

___

### Other Energy Projects

- Benefit of solar panels
	- How much electricity do you save with solar panels
		- Weather data for major cities
		- Average electricity use for someone in those major cities
			- data sources: hourly data for utility providers
				- how many households are served by that provider (within the major city)?
				- how does electricity demand change across the region serviced by the utility demand?  Some regions must require more energy than other
				- Prorate hourly data to estimate hourly demand for a single household

- https://zenodo.org/record/3473478
	- Hourly Energy Use by Region (2018)
- https://catalog.data.gov/dataset/hourly-energy-emission-factors-for-electricity-generation-in-the-united-states-4148c
	- Emission Factor for Electricity Generation
- https://openei.org/datasets/files/961/pub/
	- Household Hourly Load Profiles by city




- Forecast hybrid vehicle sales vs gasoline vehicle sales in the US
	- How does this affect CO2 emissions?