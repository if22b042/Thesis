If I use pre-existing Flood Risk data here are the following things to consider.
To train the AI I need to create a .csv file containing the features and the target.
An area which is analyzed should be about 500x500.

Features:
Static Flood Risk: GeoTiff
Rain fall in the past day
total rainfall past 10 days
rainy days past 10 days 
River flow current data
Terrain make up in percentages
    -Urban
    -Forest
    -Agricultural
    -Open
Temperature Average last 24h
Month
Latitude

 

 

Step by Step:

1. So basically I need to get the global data for GeoTiff and download all the risk projection for europe. 
2. I need to get the land data make up for all of europe (ideally a lightweight option). !!This will be done using an API (needs to somehow be adjusted for the entire square)!!
3. Then I need to get the data of each flooding event in europe in the past few years.
4. Then I will create a system which stores events where the floods happened and also invents ones that did not exist. This can either work by using data for the same location with just the (not too soon in the future)date changed.
    Structure of preliminary dataset: Date, Coodinates(Square), Flood(Yes/No), 
5. I need to find the information for each station closest to this in europe of rivers and their wateflow (or excess) for the time frame of the flooding events or those that did not happen. This will require just the info for the neares station
on the exact date. 
6. I hope there is a python library for getting the weather data for dates and locations or any API can be used for that matter.
7. Finally I run a code which takes all these events and finds the respective data and stores it in a csv


Data Sets:
Flood Risk: https://data.jrc.ec.europa.eu/dataset/1d128b6c-a4ee-4858-9e34-6210707f3c81
