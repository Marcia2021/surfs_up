# Surfs_Up Analysis

## Overview of the Surfs_Up

In this Module, in order to help W. Avy to find the best place to open a surf shop in Oahu, we used SQLAlchemy dependency in Python to connect to SQLite database. Then analyzed the weather data by converting each table in the database to Python DataFrame. Conducted statistical analysis to get the minimum, maximum and average value of precipitation and temperature, as well as the station with the highest number of data collected.  

In this additional analysis, we are going to get the temperature data for the months of June and December across all years and stations in Oahu. There are two tasks:

-	Determine the summary statistics for June in all years
-	Determine the summary statistics for December in all year.

## Analysis

1.	Imported Dependencies, Python SQL toolkit and Object Relational Mapper.

    ![inst1](https://user-images.githubusercontent.com/79289806/115977206-cf0c1700-a543-11eb-90f1-851d383f38af.png)

2.	Used create_engine() function to set up the database. Reflected database and tables. Created a session link from Python to database.

    ![inst2](https://user-images.githubusercontent.com/79289806/115977207-cf0c1700-a543-11eb-8b54-7d2c682b984f.png)

3.	Determine the summary statistics for June in all years. 

    (1) 	Filtered the Measurement table by date to retrieve the temperatures for the month of June.

    ![inst3](https://user-images.githubusercontent.com/79289806/115977208-cf0c1700-a543-11eb-8ade-f13cae87956e.png)

    (2) 	Converted the temperature data from step(1) to a list.

    ![inst4](https://user-images.githubusercontent.com/79289806/115977209-cf0c1700-a543-11eb-946c-0f19afc5a356.png)

    (3) 	Used pd.DataFrame() to create a dataframe that contains the temperatures in June. 

    ![inst5](https://user-images.githubusercontent.com/79289806/115977210-cf0c1700-a543-11eb-882b-b47f069014a7.png)

    (4) 	Used describe() function to get the statistical analysis outputs.

    ![inst6](https://user-images.githubusercontent.com/79289806/115977211-cfa4ad80-a543-11eb-90e8-ccf243e79e9d.png)

4.	Determine the summary statistics for December in all years. 
    Used similar process as the analysis for June.

    ![inst7](https://user-images.githubusercontent.com/79289806/115977212-cfa4ad80-a543-11eb-9291-199353631906.png)

## Results

1.	summary statistics for June:

    (1) 	the Dataframe for June temperature:

    ![inst8](https://user-images.githubusercontent.com/79289806/115977213-cfa4ad80-a543-11eb-852c-611e25e3c6f0.png)

    (2) 	Summary statistics for June:

    ![inst9](https://user-images.githubusercontent.com/79289806/115977214-cfa4ad80-a543-11eb-97b5-c8a5d64c659c.png)

2.	summary statistics for December:

    (1) 	the Dataframe for December temperature:

    ![inst10](https://user-images.githubusercontent.com/79289806/115977200-ce738080-a543-11eb-8a56-69648aad7701.png)

    (2) 	Summary statistics for December:

    ![inst11](https://user-images.githubusercontent.com/79289806/115977201-ce738080-a543-11eb-934a-874cbab744b3.png)

3.	Based on the summary statistics comparison between June and December across all years and stations, we could have the following conclusions.  

    ![inst12](https://user-images.githubusercontent.com/79289806/115977202-ce738080-a543-11eb-9e3e-16af5138ee67.png)

    (1) 	Across all the years and stations, there are 1700 data collected in June, 1517 data collected in December. June is a more active month compared to December for the               each of these stations to collect data.

    (2) 	The standard deviation is a measure of the amount of variation or dispersion of a set of values. The STDs from the table above are 3.257417 and 3.745920 in June and             December respectively. The higher the standard deviation, the values are more spread-out. Since December has a higher STD compared to June, the temperatures in                   December are more spread-out than June. 

    (3) 	The mean temperatures are 74.944118 and 71.041529 in June and December respectively. The mean value in June is higher than the value in December. Given that the                 standard deviation in June is lower, and the min and max temperature in June are higher compared to the values in December, we could conclude that the overall                   temperature in June is higher than December. 

## Summary: 

From the summary statistics analysis above, the overall December temperatures are lower than the temperatures in June. However, based on the differences of mean, min, and max temperature between these two months across all the years and stations, the difference is not very significant. Further analysis with other weather data element might needed.

Here are two additional queries to gather more weather data for June and December:

1.	Precipitation scores between June and December:

    ![inst13](https://user-images.githubusercontent.com/79289806/115977203-ce738080-a543-11eb-9ba2-f11d5466ed7c.png)

    We could get the summary statistics:

    ![inst14](https://user-images.githubusercontent.com/79289806/115977204-cf0c1700-a543-11eb-968f-4f76e32699be.png) 

    Compared to June, December has more precipitation across all year and stations. 

2.	The Most active station in June and December.

    ![inst15](https://user-images.githubusercontent.com/79289806/115977205-cf0c1700-a543-11eb-9554-e93e9343115b.png)         

    The station with the highest number of data collection in June and December is different. 

    Additionally, we could get the precipitation information from the most active station in order to narrow the location that best meet the expectation.
