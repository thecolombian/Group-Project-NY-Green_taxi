# NYC Taxi Impact
## Team Members
**Jorge Reyes**<br />
**Megan O'Connor**<br />
**Valdeir Faria F**<br />
**Aysenyr Teyfur**<br />

## Project Overview
Our goal with this project is to understand traffic and congestion patterns, fare and revenue trends within New York City for Green Taxis to uncover travel behavior before the pandemic when public transportation was heavily used.

### Project Questions
- Is trip length a good indicator of tip amount?
- Is there a statistically significant difference bewtween trip demand on weekends and weekdays?
- Is trip distance a good indicator of trip duration?

### Index
- [Green Taxi: Ride Duration Analysis](ADD LINK TO CODE)
- [Green Taxi: Tip Behavior](ADD LINK CODE)

[Presentation](ADD HYPERLINK)

## Description of Data Sources
- [NYC Taxi - Green Taxi Data](https://learn.microsoft.com/en-us/azure/open-datasets/dataset-taxi-green?tabs=azureml-opendatasets): Taxi data for green taxis in NYC
- [NYC Taxi - Yellow Taxi Data](https://learn.microsoft.com/en-us/azure/open-datasets/dataset-taxi-yellow?tabs=azureml-opendatasets): Taxi data for yellow taxis in NYC
- [NYC Taxi Zones](https://data.cityofnewyork.us/Transportation/NYC-Taxi-Zones/d3c5-ddgc): Taxi zone data containing names of the neighborhoods and boroughs.

### Data Exploration
The team started with the Green Taxi dataset and added the additional Yellow Taxi data to do some comparative analysis. The Taxi Zone data was added to provide more granular information about trip routes. These datasets were cleaned by removing dupliate rows and dropping unnecessary and empty columns. 

## Technologies Used
We used a variety of different technologies and libraries for this project.<br />
- **Data Transformation** Python(pandas, datetime, dateutil), Jupyter Notebook, csv file<br />
- **Analysis** Python (pandas, matplotlib, seaborn, scipy.stats), Jupyter Notebook, csv file<br />

## Data Transformation
This dataset contains 923,257 rows of data. It was filtered between 2018-05-01 and 2018-06-06. Several columns had null values due to being discontinued throughout the years. Additional columns were created to clean and provide additional date and time information. Binned data was also produced to create categorical variables for measurement variables.

## Data Analysis
### Ride Duration Analysis
In analyzing if there was a statistically significant difference between trip demand on weekends vs weekdays, it was found there is likely a difference. Through regression analysis, it was found that trip distance could have been a better indicator of how long it the taxi ride would be, likely due to the varying traffic throughout the day and night in New York.<br />
<br />
On average, a taxi ride is 23 minutes. Riders traveling at 6 am have high expected travel times. During the week those average travel times add roughly 7 minutes to the morning commute. Afternoon travel times deviate from the average between 2 pm and 4 pm but add 3 to 4 minutes to the expected travel time.<br />
![average taxi ride duration](Green-Taxi-Only-Analysis/output_data/Average-Trip-Duration_3-graphs.png)
This is quite impressive that despite the high afternoon demand, average taxi ride times are still generally quite low. The graphs below highlight taxi demand for different times and days of the week. The darkness in the heatmap highlights the heavy demand between 2 pm and 7 pm. When comparing the two heatmaps, one can see that despite the demand lasting until 7pm, the average duration of the rides begins to decrease around 5pm. More information on why average trip times decrease around 7 pm is given from the heatmap of Average Trip Distance by Hour and Day of the Week. In the evening, trip distance begins to decrease. In the mornings and during the workday, average trip distances are higher than the average of 3 miles, peaking at 5.5 miles between 5 am and 7 am on weekdays.<br />
![taxi usage](Green-Taxi-Only-Analysis/output_data/Taxi-Usage_3-graphs.png)

#### Between Borough Demand
When looking at travel between different boroughs, popular routes are those from Brooklyn to Manhattan, Manhattan to the Bronx, and Queens to Manhattan. Demand for the route from Brooklyn to Manhattan relatively stable throughout the day, calming down around 2am and picking up around 7am, despite the average trip distance being one of the highest of the most popular between borough travel routes at 14.5 miles. When looking at demand by day of the week, there is a higher demand on the weekend than during the week, especially on Saturdays to go from Brooklyn to Manhattan which aligns with the increased demand in the later hours of the day, as people may be going to Manhattan for the nightlife.<br />
<br />
Manhattan to the Bronx is the next most popular route, even though the average travel distance is 4 miles. Demand picks up throughout the day, peaking between 6pm and 8pm and slowly calming down around midnight. Looking at demand throughout the week shows that this route is more likely to be traveled between Tuesday and Saturday.<br />
<br />
The third most popular between borough route is that from Queens to Manhattan, where most of the demand is between 7am and 1pm. This route has a high remand throughout the week, with the highest demand on Saturday.<br />
The reverse trip demand does not align with the number of rides requested for these routes. For example, the demand for taxi rides from Brooklyn to Manhattan has the highest remand outside of within borough travel. However, there are few trip requests from Manhattan to Brooklyn, indicating that other means of transportation are used to travel back to the pickup location or other means of transportation were used to get to the initial pickup location.<br />
![Ride Analysis Between Boroughs](https://github.com/thecolombian/Group-Project-NY-Green_taxi/blob/moconnor/output_data/Ride-Analysis-Between-Boroughs.png)
##### Popular Drop Off Neighborhoods in Manhattan
There are several neighborhoods that are close to one another that are popular drop off neighborhoods: Harlem (Central, Central North, East North, and East South), Morningside Heights, Upper East Side North, Upper West Side North, Hamilton Heights, and Washington Heights South. All of these locations are on the north side of Manhattan.<br />
<br />
When looking at trips closer from Brooklyn to Manhattan, the most popular drop off locations are Tribeca/Civic Center, the Lower East Side, and East Village. Tribeca has a large demand between 8am and 8pm. For the Lower East Side and East Village, most riders are getting rides over in the evening and into the late night, where demand slowly begins picking up at 4pm and slowing down around 3 am. On the weekend, the most popular destinations are the East Village, the Lower East Side, and Little Italy. For riders looking to go to Little Italy, most are looking to go between 8am and 7pm. During the week, the most popular destination is Tribeca/Civic Center. 

### Tipping Behavior
As expected, tipping behavior varies by the distance traveled, with the average tip being higher the further you travel. Time of day and day of the week have less to do with the average tip, as shown when creating a simple linear regression model with using each variable. Both had r-squared values close to 0, meaning that they explained little about the variation in the expected tip amount for taxi rides. <br />
![tipping behavior by time of day and day of the week](https://github.com/thecolombian/Group-Project-NY-Green_taxi/blob/moconnor/output_data/Tipping-Behavior-by-Day-of-Week-and-Time-of-Day.png)

### Most common payment method for green taxis and yellow taxis

### Green compared to yellow - overview of findings

### Boroughs for green taxis vs yellow taxis

## Presentation
PowerPoint Deck summarizing our project: [Presentation] (NYC_Taxi_Impact_Presentation.pdf)

## Resources
### Analysis Files
- [Green Taxi: Ride Duration Analysis](ADD LINK TO CODE)
- [Green Taxi: Tip Behavior](ADD LINK CODE)
### Images
- [output_data](ADD LINK CODE)
