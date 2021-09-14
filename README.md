# Tranzmeo_Machine_Test

## Part 1
Given [latitude_longitude_details.csv](input_files/latitude_longitude_details.csv) as a list of latitude and longitudes route from Point A to Point B

1. Write a python code to find the latitude and longitude coordinates that are out of route and automatically fix the same to form a continuous path.
#### Solution file : [Part_1_1_latitude_longitude_route_fix_solution.ipynb](solution/Part_1_1_latitude_longitude_route_fix_solution.ipynb)
#### Output file : [latitude_longitude_corrected_details.csv](output_files/latitude_longitude_corrected_details.csv)
#### Short Explanation:
Used the OSRM API to find the nearest driving location for input latitude and longitude. The response will get the nearest driving location with coordinates. Used plotly_express to visualize the coordinates as in Map view.
2. From the given terrain list with kilometers, write a python script to generate DB of each latitude and longitude pair with matching terrain information (NB: take the starting latitude and longitude and 0 KM and end as )
3. Write Query to list all the points with terrain “road” in it without “civil station”

## Part 2
1. Generate a set of points which are 25 meters to the left and right of the given latitude and longitude, Use multi-threaded/ multi-processing to optimize the execution with the reasoning of the same
#### Solution file : [Part_2_1_new_distance_added_coordinates_pair_solution.ipynb](solution/Part_2_1_new_distance_added_coordinates_pair_solution.ipynb)
#### Output file : [new_distance_added_coordinates.csv](output_files/new_distance_added_coordinates.csv)
#### Short Explanation : 
First find the meter per degree for earth, as we have already earth radius details.<br>
The find new coordinate point 25 meter <br>
to right => longitude + (meters_add * meter_per_degree) / cos(latitude * (pi / 180)) <br>
for left => longitude - (meters_add * meter_per_degree) / cos(latitude * (pi / 180)) <br>
The reason for multiplying pi/180 is to convert the degree to radians. <br> <br>
2. Design a data structure that can, efficiently with respect to time used, store and check if the total of any three successively added elements is equal to a given total.
For example, MovingTotal() creates an empty container with no existing totals. append([1, 2, 3, 4]) appends elements [1, 2, 3, 4], which means that there are two existing totals (1 + 2 + 3 = 6 and 2 + 3 + 4 = 9). append([5]) appends element 5 and creates an additional total from [3, 4, 5]. There would now be three totals (1 + 2 + 3 = 6, 2 + 3 + 4 = 9, and 3 + 4 + 5 = 12). At this point contains(6), contains(9), and contains(12) should return True, while contains(7) should return False.
#### Solution file : [Part_2_2_solution.ipynb](solution/Part_2_2_solution.ipynb)
