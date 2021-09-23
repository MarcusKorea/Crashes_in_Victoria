# project-1
# Does weather impact accident counts in Victoria Australia?
### Contributors: Ivana, Marcus, Sanuli and Tamer 

### Why? 
Want to see if we can predict the accident count using the amount of rainfall or temperature.
## Hypotheses
- Expect a higher frequency of road accidents frequency in Melbourne LGA compared to other.
- Expect an increased frequency of road accidents during weekdays.
- Increased accidents frequency during wet weather.
- Increased accident frequency during cold weather. 
## Data Collection
### VicRoads Open Data - Road Crashes (2014-2019)
- CSV file (77,513 rows)
- Removal of unrelated columns
- Removal of NaN values
- https://vicroadsopendata-vicroadsmaps.opendata.arcgis.com/

### Bureau of Meteorology 
- CSV files (daily)
- Concatenated dates
- Merged rainfall + temperature
- http://www.bom.gov.au/climate/data/ 

### Google API
 - To create a heat-map
 - https://developers.google.com/maps

## Analysis
- Data analysis undertaken using Jupyter Notebook with the input being the cleaned data as CSV file from previous step.
### Road Accidents by area
- Created a Jupyter notebook to analyse accidents per LGA
- Created a pie chart to show frequency of accidents in country vs metropolitan areas
- Created a bar chart to show frequency of accidents in LGA's that had more than 2000 accidents
### Road accidents compared to days of the week
- Created a bar chart to show rate of accidents per day of the week
- Created a bar chart to show rate of accidents per hour of selected days
- Looked at the mean value of accident counts at 12am and compared to 12am accident count on Sunday
### Rainfall vs Accident Count
- Due to time constraints, we focused on weather data for Melbourne and Hume
- Created scatter plots and regression lines for accidents count in both all roads and fast/arterial roads vs rainfall
- Did the same for fatalities sum vs rainfall 
- Did hypothesis testing for all cases
### Temperature vs Accident Count
- Created scatter plots and regression line for accidents count in both all roads and fast roads vs temperature
- Did hypothesis testing for both cases

## Conclusion
### Road Accidents by area
- Did the Melbourne area have a higher accident count?
- Victoria had 71003 total accidents
- Melbourne had 3897 total accidents
- Hume had 2298 accidents 
- Metro Victoria had 50308 total accidents (69.3% of all accidents)
- Hypothesis appears to be supported
### Road accidents compared to days of the week
- Were we correct? Not exactly
- Increase in accidents as the week goes on
- Sunday was the day when most accidents happen (highest accident count occurring at 12 pm)
- Curiously Saturday had a significant drop in accidents
- Sunday 12 am accident counts had a 120 increase from the mean 12 am accident count rate (Why?)
- Could people being staying out past 12 am on a Saturday night?
### Rainfall vs Accident Count
- Did rainfall actually correlate to accident counts? No

### Accident Count Vs Rainfall (Melbourne) 
- Almost No correlation (r value of 0.002)
  - p-value = 0.1

### Accident Count Vs Rainfall ( Arterials/Freeways in Melbourne)
- Almost No correlation (r value of 0.04)
  -p-value = 0.195

### Accident Count Vs Rainfall (Hume) 
- Almost No correlation (r value of 0.03)
  - p-value  = 0.263

### Accident Count Vs Rainfall ( Arterials/Freeways in Hume)
- Almost No correlation (r value of 0.5)
  - p-value = 0.157

### Temperature vs Accident Count
- Did temperature actually correlate to accident counts? No

### Accident Count Vs Temperature (Melbourne) 
- Almost No correlation (r value of 0.05)
  - p-value = 0.061

### Accident Count Vs Temperature ( Arterials/Freeways in Melbourne)
- Almost No correlation (r value of 0.04)
  - p-value = 0.125

### Accident Count Vs Temperature (Hume) 
- Almost No correlation (r value of -0.02)
  - p-value  = 0.513

### Accident Count Vs Temperature ( Arterials/Freeways in Hume)
- Almost No correlation (r value of 0.02)
  - p-value = 0.507
The tests run all showed values above 0.05, suggesting that there was no correlation between the variables we test. Note: The p-value for accident count vs Temperature was 0.06, which is very close to 0.05.

### Conclusion for rainfaill and temperature variabels vs accident counts (looking at them seperatly)
- Maybe a multiple linear regression (using both rainfall and temperature) can be used to help predict accident counts (or even include other vairbales). 


## How to redo the analyse using out files
- Each notebook is labeled as a 'step', please run them in order. The code should run smoothly if run once in order.
- The figures are stored as screenshots in the figures folder and are named appropiatley.
- The raw data files are found in the folder 'raw_data'
- The cleaned data sets are stored in 'cleaned_data' (This also includes the merged data).
- Files should not be moved.
- In the weekends notebook (step 5), there are some user defined functions that can be used, instructions are included
- When running step9 notebook, please copy and paste your own GoogleAPI key in the config file
