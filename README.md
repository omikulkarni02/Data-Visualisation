	
# Dataset 
•	Dataset was retrieved from Kaggle website. It is a countrywide accident dataset which covers 49 states of United States of America. Two research papers were published using this dataset to make prediction for real time accidents. 

•	Data present in Dataset is from February 2016 to March 2019 and contains 2.25 Million records. There are total 49 columns and 2.25 Million rows in dataset. 

•	Data was collected using several data providers, including two API which provide streaming traffic event data. Total size of the csv file on the disk is 819MB.

•	Some of the important attributes in dataset are: Severity, Latitude, Longitude, time of accident, State, City, Street, Traffic_signal, weather, visibility, windspeed. Data contains multiple datatypes including float, Boolean, integer and object. 

•	There are two aspects of Big Data present in dataset which are Volume (as it contains 2.25 million rows) and Variety (as it contains 49 different attributes)  

# Data Exploration, Processing, Cleaning and/or Integration 

As the aim of my visualization assignment was to show the trend of accidents in US States and how it has increase over the years, so I selected only certain attributes from the overall dataset and created a new dataframe. Then, to get the clean data, I used dropna() function to delete all null values. Now the dataframe was clean and ready to perform specific operations according to graph type.
# For Choropleth Map:
•	To show the distribution of accidents occurred in US States, choropleth map was used. 

•	I added a new column to dataframe which contained the count of occurrence of each State in the dataset.

•	Distinct States and its corresponding occurrence values was used to build a choropleth map.

# For Timeseries Graph:
•	This graph shows distribution of accidents month wise spread across the years. X axis is taken as Month of the year and Y axis stands for overall accident rate. The line graph shows the Year.

•	There was no explicit year and month column present in the dataset. It was derived from the Start Time column of the dataset.

•	Then for each month of each year, the occurrence of accident was calculated and stored in new columns

# For Animated Bubble graph:
•	This bubble graph shows how accident rates increased in States from 2016 to 2018 through animation

•	3 different dataframes were created which contained data from 2016,2017 and 2018 respectively

•	Count of each state was taken and all other duplicate rows were deleted

•	Then these 3 dataframes were joined using pandas ‘concat’ command

•	Bubbles size showed the count of accidents in that state 

# Visualisation 
# I.	Choropleth Map
•	Data contains accident information which is spread across every state in United States, hence to determine total accident cases in each state Choropleth map was used to visualize this information

•	Red colour scale was used as the information contained accident data

•	Lower the accident rate, faint the shade and higher the accident rate, dark the shade

•	Map was constructed using plotly library 


# II.	Time Series Graph
•	As the data of accidents was collected from 2016 to early 2019, plotting time series helped us to understand how the accident rate has increased year by year

•	Dividing the data into month wise shows which month had most occurrence of accidents

•	Each year is represented as a line graph and is differentiated by distinct colours

•	Plotly’s graph_obj library was used to plot this graph


# III.	Animated Bubble Plot 
•	This animated bubble plot shows how accident in every state has grown year by year

•	Each bubble represent distinct states and they are differentiated by colour coding

•	Size of bubble depends on the number of accidents; hence the size of bubble increases as the number of accidents in that state increase.

•	X axis denotes the frequency of accidents by state and Y axis has total accident frequency
