# sweep_analysis
Analysis of data from a sweep of a bike/pedestrian path model that forecasts improvements in 
different health outcomes (diabetes, high blood pressure and poor physical health).
Data is organized based on census tract in the City of Norfolk, VA. 
Results to be used to inform decisions of public officials. 

bike_ped_model_sweep: 
Results of sweep on model. Model is not part of project. 
Data from 51 census tracts, organized by health outcome. Provides current state of the health outcome and the minimum, median and maximum improvement forecasted by 
the model for each added mileage (starts at 0.25 and adds 0.05 miles at a time to 2.00 miles)

sweep_analysis.mlx
  sm_mile4max: 
  Finds the smallest amount of miles added to the tract to get the highest improvement in the given health outcome.
  Informs urban planners, politicians on most efficient mileage to add to each tract to effect a particular outcome. 

  sm_mile4any: 
  Finds the smallest amount of miles added to the tract to get any improvement. Some tracts will have no improvement regardless of miles added.

  bot_ and top_ tracts: 
  These are the bottom and top (respectively) tracts for each health outcome. The current state variable is positive, meaning that the higher the number the better (i.e. healthier) that tract is. 

Portfolio.mlx
  sm_mile4max_matrix.csv: 
  The sorted version of sm_mile4max wherein the tracts are sorted with the tracts with the worst current state of each health outcome at the top and their associated values sorted accordingly. Quartet of columns contains the Tract number, the current state, maximum possible improvement and the miles added to acheive this improvement. There are 12 columns total, four for each health outcome. 
  
  best_portfolio: 
  Comparing the max improvement values, the maximum improvement for each row (from the sm_mile4max_matrix) is selected and the corresponding number of miles is added to a portfolio along with the tract number and the improvement. No tract has more than 2 miles added to it, and a 1 point improvement is considered equal in every category. Every iteration involves a series of checks to make sure that the correct value is selected, to see if the tract has already been added to the portfolio (if it has, there is a secondary check to compare the two values and select the value of miles that corresponds to the largest improvement), and to make sure that the selected value isn't an empty array.  
  
  best_portfolio_health outcome_package size: 
  The best portfolio for a given package size for each health outcome. Packages range from 1 to 25 miles, no tract has more than 2 miles added.
