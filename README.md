# sweep_analysis
Analysis of data from a sweep of a bike/pedestrian path model that forecasts improvements in 
different health outcomes (diabetes, high blood pressure and poor physical health).
Data is organized based on census tract in the City of Norfolk, VA. 
Results to be used to inform decisions of public officials. 

bike_ped_model_sweep: 
Results of sweep on model. Model is not part of project. 
Data from 51 census tracts, organized by health outcome. Provides current state of the health outcome and the minimum, median and maximum improvement forecasted by 
the model for each added mileage (starts at 0.25 and adds 0.05 miles at a time to 2.00 miles)

sm_mile4max: 
Finds the smallest amount of miles added to the tract to get the highest improvement in the given health outcome.
Informs urban planners, politicians on most efficient mileage to add to each tract to effect a particular outcome. 

sm_mile4any: 
Finds the smallest amount of miles added to the tract to get any improvement. Some tracts will have no improvement regardless of miles added.

