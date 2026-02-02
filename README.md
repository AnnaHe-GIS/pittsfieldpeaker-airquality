This readme file was generated on [2026-02-02] by [AnnaHe]

*Note:
[text within square brackets should be changed to specific information about your dataset.]
*help text within asterisks should be deleted before finalizing your document**

# GENERAL INFORMATION

* Title of Project:
## Author/Principal Investigator Information
Name: Anna He
ORCID:
Institution: Harvard University School of Public Health
Address: 
Email: anna_he@harvard.edu

## Author/Associate or Co-investigator Information
Name: 
ORCID:
Institution: 
Address: 
Email: 

## Author/Alternate Contact Information
Name: 
ORCID:
Institution: 
Address: 
Email: 

* Date of data collection: *provide single date, range, or approximate date; suggested format YYYY-MM-DD)*
* Geographic location of datasets: Pittsfield, MA 
* Information about funding sources that supported the collection of the data: 


# SHARING/ACCESS INFORMATION

* Licenses/restrictions placed on the data: 
* Links to publications that cite or use the data: 
* Links to other publicly accessible locations of the data: 
* Links/relationships to ancillary data sets: 
* Was data derived from another source?
	* If yes, list source(s): 
* Recommended citation for this dataset: 


# DATA & FILE OVERVIEW

## File List: *list all files (or folders, as appropriate for dataset organization) contained in the dataset, with a brief description*

### Raw: 
* clarity_sensor_data_240401_250930.csv 
	* Description: Time-series air quality data from BEAT sensors from April 1, 2024 through September 30, 2025.
	* Download Source: BEAT Clarity Dashboard
* peaker-hourly-emissions-240401-250930.csv 
	* Description: Hourly emissions for peaker power plant in Pittsfield, MA from April 1, 2024 through September 30, 2025.
	* Download Source: EPA CAMPD 
* peaker.csv  
	* Description: Pittsfield peaker plant ID and latitude/longitude.
	* Download Source: EPA CAMPD
* WeatherRaw.csv 
	* Description: Hourly dry bulb temperature, hourly humidity, and hourly wind speed data for federal sensor at Pittsfield Municipal Airport.
	* Data Source: National Centers for Environmental Information - U.S. Local Climatological Data (LCD) 
* sensors_raw.csv 
	* Description: Names, descriptions, and latitude/longitudes for BEAT sensors.
	* Data Source: Latitude/longitudes taken from BEAT Clarity Dashboard. Names/Descriptions taken from BEAT sensor location Google spreadsheet. 

### Cleaned inputs: 
* sensordata_clean.csv 
	* Description: Time-series air quality data with only relevant columns from BEAT sensors from April 1, 2024 through September 30, 2025.
	* Processed from: clarity_sensor_data_240401_250930.csv 
	* Processing: Removed unneeded columns. 
* peakerop_clean.csv
	* Description:  Cleaned hourly emissions for peaker power plant in Pittsfield, MA from April 1, 2024 through September 30, 2025. Includes additional columns needed for data analysis.
	* Processed from: peaker-hourly-emissions-240401-250930.csv 
	* Processing: Standardized formatting for date and hour; creaed new binary columns for operating (1/0) and operating_f (Yes/No); added year, month, day season, time of day, and weekday (binary - 1/0).
* WeatherClean.csv
	* Description: Cleaned hourly dry bulb temperature, hourly humidity, and hourly wind speed data for federal sensor at Pittsfield Municipal Airport.
	* Processed from: WeatherRaw.csv 
	* Processing: Removed unneeded columns; renamed columns to a standardized format. 
* sensors.csv 
	* Description: Names, descriptions, latitude/longitudes, distance to the peaker (m), distance to the airport (m), distance to MassDOT major roads for BEAT sensors.
	* Processed from: sensors_raw.csv 
	* Processing: Added new columns and calculated the distance from each sensor to the peaker plant, to the Pittsfield Municipal Airport, and to major roads. Calculated the bearing (orientation) of each sensor (in degrees and in radians) relative to the power plant, where 0 degrees is directly North. Calculated sin and cos of bearings for potential use in models. 

### Outputs:  
* sensors_joined_all.csv 
	* Description: Time series air quality data for each sensor with associated peaker operations and weather data from April 1, 2024 to Sept 30, 2025.
	* Processed from: sensordata_clean.csv, peakerop_clean.csv, WeatherClean.csv, sensors.csv 
	* Processing: Joined the time series sensor air quality data with peaker plant, weather, and sensor description data using either a common year;day;date;hour column or a common data source ID column.
* sensors_summer.csv
	* Description: Summer 2024 and Summer 2025 only -- Time series air quality data for each sensor with associated peaker operations and weather data. 
	* Processed from: sensors_joined_all.csv
	* Processing: Filtered sensors_joined_all.csv to only the summer months (June, July, August)
* allendale_aq.csv
	* Description: Summer 2024 and Summer 2025 only -- Time series air quality data for the sensor at Allendale Elementary with associated peaker operations and weather data. 
	* Processed from: sensors_summer.csv
	* Processing: Filtered sensors_summer.csv to only the sensor ID at Allendale Elementary.




* Relationship between files, if important: 
* Additional related data collected that was not included in the current data package: 
* Are there multiple versions of the dataset?
	* If yes, name of file(s) that was updated: 
	* Why was the file updated? 
	* When was the file updated? 


# METHODOLOGICAL INFORMATION

## Description of methods used for collection/generation of data: 
*include links or references to publications or other documentation containing experimental design or protocols used in data collection*

## Methods for processing the data: 
*describe how the submitted data were generated from the raw or collected data*

## Instrument- or software-specific information needed to interpret the data: 
*include full name and version of software, and any necessary packages or libraries needed to run scripts*

*include any additional methodological information needed to interpret and/or use the data, as appropriate*
* Standards and calibration information, if appropriate: 
* Environmental/experimental conditions: 
* Describe any quality-assurance procedures performed on the data: 
* People involved with sample collection, processing, analysis and/or submission: 


# DATA-SPECIFIC INFORMATION FOR: [FILENAME]
*repeat this section for each dataset, folder or file, as appropriate*

* Number of variables: 
* Number of cases/rows: 
* Variable List: *list variable name(s), description(s), unit(s) and value labels as appropriate for each*
* Missing data codes: *list code/symbol and definition*
* Specialized formats or other abbreviations used: 
