# power-demand-clustering
Analysed power demand data from substations through hierarchical clustering.
____________________________________________________________________________

Check the .html doc for rendered output of the .ipynb file.
You can run the .ipynb file on jupyter notebook, make sure it is in the same folder as all the data files.

AIM
The aim of this analysis is to perform clustering on power data recordings at substations in order to see whether there are groups that have similar demand profiles and to see whether there are differences between years.

DATA
There are two types of data: (i) variable - the measurements from the monitors; and (ii) fixed - characteristics of the substations, that include information that may be useful when trying to understand and name your clusters.
There are three datasets containing the variable data, each corresponding to a different year.
• January_2013.RData • January_2014.RData • January_2015.RData
You can load each dataset using R’s load function.
These datasets contain data for the same 535 substations. Each row of a dataset represents a day’s recording at a given substation, on a particular date. The first two columns indicate the date and Substation ID. The remaining 144 columns indicate the raw power data recorded by monitors at 10 minute intervals throughout the day.
The fixed data is in the Characteristics.csv file. This contains the fol- lowing information:
• SUBSTATION_NUMBER - so you can link with the variable data
• TRANSFORMER_TYPE - ground or pole mounted (indicating urban or rural substations)
3
• TOTAL_CUSTOMERS - the number of customers receiving their electricity from this substation
• Transformer_RATING - indicates the total power being delivered by the substation
• Percentage_IC - the percentage of industrial and commerical (not domes- tic) customers
• LV_FEEDER_COUNT - the number of feeders coming from the substation
• GRID_REFERENCE - the Ordnance Survey grid reference for the location.
(See https://getoutside.ordnancesurvey.co.uk/guides/beginners-guide-to-grid-references/ for information, if you wish to use this information but it is not obligatory
to do so.)
