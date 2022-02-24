# San Francisco Housing Market Project

## Purpose of this project:

**Use data visualization skills to find real estate investment opportunities in San Francisco**

### First Analysis: Identify trend patterns in the number of Housing Units in the area

* Was able to find this trend by slicing the data down to two columns, housing units and years: 

`housing_units_by_year = sfo_data_df[['housing_units', 'year']]`

* Next, used the `groupby` function to calculate the mean number of housing units for each year:

`housing_units_by_years = housing_units_by_year.groupby('year').mean()`


