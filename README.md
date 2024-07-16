# NYC Taxi Impact
## Team Members
**Jorge Reyes**
**Megan O'Connor**

## Project Overview
Our goal with this project is to understand traffic and congestion patterns, fare and revenue trends within New York City for Green Taxis.

### Project Focus
(why is this important?)

### Index
[nice to have]

![Presentation](HYPERLINK)

## Description of Data Sources
- ![NYC Taxi - Green Taxi Data](https://learn.microsoft.com/en-us/azure/open-datasets/dataset-taxi-green?tabs=azureml-opendatasets): Taxi data for green taxis in NYC
- ![NYC Taxi - Yellow Taxi Data](https://learn.microsoft.com/en-us/azure/open-datasets/dataset-taxi-yellow?tabs=azureml-opendatasets): Taxi data for yellow taxis in NYC
- ![NYC Taxi Zones](https://data.cityofnewyork.us/Transportation/NYC-Taxi-Zones/d3c5-ddgc): Taxi zone data containing names of the neighborhoods and boroughs.
The data was filtered between 2018-05-01 and 2018-06-06.

### Data Exploration
The team started with the Green Taxi dataset and added the additional Yellow Taxi data to do some comparative analysis. The Tazi Zone data was added to provide more granular information about trip routes. These datasets were cleaned by removing dupliate rows and dropping unnecessary and empty columns. 

## Technologies Used
We used a variety of different technologies and libraries for this project.
**Data Transformation** Python(pandas, datetime, dateutil), Jupyter Notebook, csv file
**Analysis** Python (pandas, matplotlib, seaborn, scipy.stats), Jupyter Notebook, csv file

## Data Transformation
This dataset contains X rows of data. The data had several columns that has null values due to being discontinued in the data collection throughout the years. Additional columns were created to clean and provide additional date and time information. Binned data was produced to create categorical variables for measurement variables as well.

## Data Analysis
### Green compared to yell - overview of findings

### Boroughs for green taxis vs yellow taxis

### Most common payment method for green taxis and yellow taxis

### Tipping Behavior
As expected, tipping behavior varies by the distance traveled, with the average tip being higher the further you travel. Time of day and day of the week have less to do with the average tip, as shown when creating a simple linear regression model with using each variable. Both had r-squared values close to 0, meaning that they explained little about the variation in the expected tip amount for taxi rides. 
![tipping behavior by time of day and day of the week]([ADD LINK](https://github.com/thecolombian/Group-Project-NY-Green_taxi/blob/moconnor/output_data/Tipping-Behavior-by-Day-of-Week-and-Time-of-Day.png))

