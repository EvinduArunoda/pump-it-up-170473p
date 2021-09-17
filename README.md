# Pump it Up : moracse_170473p

## Pre processing & Feature Engineering 

### Handling Missing Values
* Features with missing values were identifies first.(0 s)
  * Missing values were identidied in these columens :  gps_height, population, amount_tsh, longitude, latitude, construction_year, scheme_name
* Then those values were replaced with 'nan'.
* Then to fill nan values, following operations were carried out.

* For the 'gps_height' column,
  * First dataset was grouped by region and district_code and then 'nan' values were replaced by mean of the gps_height.
  * Then dataset again grouped by region and then 'nan' values were replaced by mean of the gps_height.
  * Then as the 3rd step, remaining 'nan' values were replaced by mean of gps_height.
  
* For the 'population' column,
  * First dataset was grouped by region and district_code and then 'nan' values were replaced by mean of the population.
  * Then dataset again grouped by region and then 'nan' values were replaced by mean of the population.
  * Then as the 3rd step, remaining 'nan' values were replaced by mean of population.

* For the 'amount_tsh' column,
  * First dataset was grouped by region and district_code and then 'nan' values were replaced by mean of the amount_tsh.
  * Then dataset again grouped by region and then 'nan' values were replaced by mean of the amount_tsh.
  * Then as the 3rd step, remaining 'nan' values were replaced by mean of amount_tsh.

* For the 'longitude' and 'lattitude' columns,
  * First dataset was grouped by region and district_code and then 'nan' values were replaced by mean of the lattitude/longitude.
  * Then dataset again grouped by region and then 'nan' values were replaced by mean of the lattitude/longitude.

* For the 'construction_year' column,
  * First dataset was grouped by region and district_code and then 'nan' values were replaced by median of the construction_year.
  * Then dataset again grouped by region and then 'nan' values were replaced by median of the construction_year.
  * Then dataset again grouped by district_code and then 'nan' values were replaced by median of the construction_year.
  * Then as the 4th step, remaining 'nan' values were replaced by median of construction_year.

* Then 3 features('amount_tsh', 'gps_height', 'population') were scaled between 0 and 20.

### Creating New Features

* New feature, 'functional_period' was created by taking time gap between, 'date_recorded' and 'construction_year'.

### Data Cleaning

* Following features were dropped.
  * scheme_name : This feature was drooped due to having too many null values.(35258)
  * 


* Then columns with Dtype object were converted into lower case.

### Preprocessing

* For preprocessing, using pd.factorize labels are encoded into categorical variables.
