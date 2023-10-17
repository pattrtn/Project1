# Project1
#### Problem Statement:
For student from research club who need to understand why her allergies worse when it rains and decide to develop a comprehensive understanding of the interplay between rain and allergies.

#### Background: 
Air pollution and climate change can promote allergies by influencing the human body and immune system, as well as the abundance and potency of environmental allergens and adjuvants.Climate parameters and air pollutants can influence the release, potency, and effects of allergens and adjuvants: 
temperature (T), relative humidity (RH), ultraviolet (UV) radiation, particulate matter (PM), ozone and nitrogen oxides (O3, NOx)

#### Objectives:
Develop a comprehensive understanding of the interplay between rain and allergies ,identify strategies for prevent or reduce allergies triggered by rain.

---

#### Datasets:

**Datasets corresponding to rainfall information:**

* [`rainfall-monthly-number-of-rain-days.csv`](./Data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* [`rainfall-monthly-total.csv`](./Data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022
* [`relative-humidity-monthly-mean`](./Data/relative-humidity-monthly-mean.csv): The monthly mean relative humidity recorded
* [`SurfaceAirTemperatureMonthlyMeanDailyMaximum`](./Data/SurfaceAirTemperatureMonthlyMeanDailyMaximum.csv): The monthly mean daily minimum temperature recorded at the Changi Climate Station
* [`surface-air-temperature-monthly-mean-daily-minimum`](./Data/surface-air-temperature-monthly-mean-daily-minimum.csv): The monthly mean daily maximum temperature recorded at the Changi Climate Station
* [`sunshine-duration-monthly-mean-daily-duration`](./Data/sunshine-duration-monthly-mean-daily-duration.csv): The monthly mean sunshine hours in a day recorded at the Changi Climate Station
* [`RelativeHumidityMonthlyMean`](./Data/RelativeHumidityMonthlyMean.csv): Monthly mean relative humidity


**Datasets corresponding to Air Quality:**
* [`air-pollutant-ozone`](./Data/air-pollutant-ozone.csv): Annual daily maximum 8-hr means for ozone (µg/m3)
* [`air-pollutant-particulate-matter-pm2-5`](./Data/air-pollutant-particulate-matter-pm2-5.csv): Annual means for PM2.5 (µg/m3)
* [`AirPollutantNitrogenDioxide`](./Data/AirPollutantNitrogenDioxide.csv): Annual means for nitrogen dioxide (µg/m3)


---

#### Data Import & Cleaning:
*Step 1 : Choose Data from data.gov.sg
*Step 2 : Import data by using Pandas
Step 3 : Check for missing values , datatype and any obvious issues
No missing value
Step 4 : Fixing and cleaning data
Change data ‘month’ to datetime type
Create new columns for month and year
Merge rain data
Merge air pollution related data
Find sum and mean for rain data
Merge rain data and air pollution data
Check and drop empty row
Save cleaned dataframes as csv files.


---

#### Data Dictionary
|Feature|Type|Dataset|Description|
|:--|:--|:--|:--|
|year|int||Year of collecting data|
|rainydays|int|rainfall-monthly-number-of-rain-days|Monthly number of rain days from 1982 to 2022 if the total rainfallis 0.2mm/day or more.|
|totalrainfall|float|  rainfall-monthly-total|Monthly total rain recorded in mm(millimeters) from 1982 to 2022|
|mean_sunshine_hrs|float|sunshine-duration-monthly-mean-daily-duration|The monthly mean sunshine hours in a day recorded|
|temp_min|float|SurfaceAirTemperatureMonthlyMeanDailyMaximum|The monthly mean daily minimum temperature recorded|
|temp_max|float|surface-air-temperature-monthly-mean-daily-minimum|The monthly mean daily maximum temperature recorded|
|rh_mean|float|RelativeHumidityMonthlyMean.csv|Monthly mean relative humidity|
|pm2.5_mean|float|AirPollutantParticulateMatterPM2.5|  Annual means for PM2.5 (µg/m3) are based on WHO Air Quality Guidelines (global update 2005).|
|o3_mean|float|air-pollutant-ozone.csv|Annual daily maximum 8-hr means for ozone (µg/m3)|
|no2_mean|int|AirPollutantNitrogenDioxide|Annual means for nitrogen dioxide (µg/m3)|
