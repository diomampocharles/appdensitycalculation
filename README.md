# appdensitycalculation
This is for the Data Science Toolbox activity of Group 8.

** Barangay Population Density **

To start with the exercise, the datasets were read and stored to corresponding variables.

The dplyr library was then loaded to gain access to several functions.

The population dataset was then grouped according to region. The 'summarise' function counted the number of times each region appeared in the dataset. This also corresponds to the number of barangays per region. This was stored in the variable 'CountPerRegionSummary'.

The population dataset was then grouped into Barangay, Region and CityProvince attributes. The PopulationPerBarangay was calculated through the summation of Population data, presented per region and arranged alphabetically with respect to the latter.

BarangayArea is the area per barangay, roughly calculated through dividing the area per region by the number of barangays per region. The regions column was obtained and binded to the respective barangay areas.

The population density was computed by dividing the PopulationPerBarangay by the BarangayArea. Results were sorted in descending order with respect to the top population density.

** City Population Density **

To get the city population density:

The team used dplyr package to execute the code.

First, the team assigned a variable to both the population.csv and regionarea.csv. Next, we grouped the region with the count of its cities using the population variable.

Second, the team grouped the region and city province each with a sum of the population using the population variable.

Third, the team divided the area of the whole region (using the regionarea variable) over the count of its cities to derive the area of a city (assuming each city in the same region has the same area). Then, the team combined the region name and the area per city into a table.

Fourth, the team used inner join function to converge the area of a city to its respective region. Then, we used mutate function to create a new column, Density, which is the quotient of population and area.

Finally, we sorted the density from highest to lowest, taking only the top 5 cities, then generated a new csv file.
