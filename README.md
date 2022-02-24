# San Francisco Housing Market Project

## Purpose of this project:

**Use data visualization skills to find real estate investment opportunities in San Francisco**

### First Analysis: Identify trend patterns in the number of Housing Units in the area

* Was able to find this trend by slicing the data down to two columns, housing units and years: 

`housing_units_by_year = sfo_data_df[['housing_units', 'year']]`

* Next, used the `groupby` function to calculate the mean number of housing units for each year:

`housing_units_by_years = housing_units_by_year.groupby('year').mean()`

* After creating the DataFrame, we used the `hvplot.bar` function to create an interactive bar chart visual:

### Second Analysis: Calculate and Plot the Average Sale Prices per Square Foot

* Started to create our Prices Per Square Foot DataFrame by grouping the entire existing SFO DataFrame by year and found the mean for each
* Then used the `drop()` function to drop the irrelevant Housing Units column from the Prices Per Square Foot DataFrame for our analysis
* After finalizing the DataFrame, we used the `hvplot.line()` function to create a line chart visual that looked at the trends between sale price per square foot and gross rent

### Third Analysis: Compared the Average Sale Prices by Neighborhood
* Took a closer look at the average sale price per square foot by using interactive widgets to slice data by neighborhood
* Started by using the `groupby[['neighborhood','year']].mean()` function to create a DataFrame that sorts the data by neighborhood and year
* Used the `.drop()` function to drop the Housing Units column from the DataFrame
* Created a line plot using the `hvplot.line()` function and included the `groupby('neighborhood')` function inside of the visual to create a widget that would allow you to see the different neighborhoods pricing data
