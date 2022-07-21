# PyBer_Analysis
# Objectve 
Pyber is a ride share company that provides services to cities with Rural, Uban and Subrban areas (city types). This report provides a summary of the services provided creating a visual picture of how frequesnt are teh services used, the number of drivers and fare averages for each city type. 

# Summary 

## Deliverable - 1 
For deliverable 1 we are asked to  provide the numberof rides, driver and toal fares for each city type. We are then tasked with generating the average fare for each ride, and the average fare per driver for each city type. To acomplish this I loaded each csv file and merged the files to the left using "city". The pyber_summary table below outlines the required information. 

**Pyber Summary Table**
![image](https://user-images.githubusercontent.com/104601282/180115926-814760c2-50b1-434d-b6a1-cce092b9d60d.png)

## Deliverable - 2
For deliverable two we are tasked with creating a multiple line graph to illustrae the total fares per week by city type using the pivot and resample functions. To acomplished the tasks given, a new DataFrame was created. The data was grouped by (groupby) date, city type, and the fare for eachfare. The index was reset using pivot. The date range was set from January 1, 2019 to April 29, 2019 using .loc. Resampling is used to split the time range into weeks (frequency) this is done by adding .resample('W').sum() as seen in the weekly_fares_data table below.

**Weekly Fares Table**
![image](https://user-images.githubusercontent.com/104601282/180120418-0094f55e-32d3-49fc-8c3b-0906ca48c1b5.png)

The resample table was used to create the line graph below. The graph was created using the object-oriented interface method and the df.plot() method, as well as the Matplotlib "fivethirtyeight" graph style code provided in the starter code. The image is saved in the analysis folder this was done using# Save Figure
plt.savefig("analysis/PyBer_fare_summary.png")

plt.show 

![image](https://user-images.githubusercontent.com/104601282/180121018-5649924d-7e20-4dec-b190-c99c1349bae1.png)


## Results

# Deliverable 3

The data shows that the majority of transports and earnings are generated in the Urban areas , followed by Suburban and Rural
- Urban: 68% of total rides
- Suburban: 23% of total rides 
- Rural: 5% of total rides 

Urban  cities have four times moredrivers than the suberban and suberban has more drivers than the urban, this is likely due to population. 

![image](https://user-images.githubusercontent.com/104601282/180132065-21f0032f-2330-4926-81f6-4060b40b6195.png)

The line graph shows spikes in fares during April for the Rural areas and a decline in fares for the same time frame in suburban areas.  

### Recomendations 

- Include population in next report to help assess the number of drivers per capita per'se
- My suggestion to better service the area is to reassign drivers from the suburban areas to the rural during April to better service these areas. 
- Continue to monitor and trend the fares per city type per week, monitor events in each city type area trend and compare to the fares summary data adjust driver counts based on expected attendance to event. 
- Offer a new hire bonus to drivers in Rural areas to help increase number of drivers
