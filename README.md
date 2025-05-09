## Introduction
#### What is HYSPLIT

#### What you will learn here

## Requirement
#### Software
1.Hysplit  
2.Meteoinfo(optional, but recommended)  
3. Python (Programming software for data analyzing and plotting) (optional)
#### data
HYSPLIT requires data in arl format, you can use:  
1.NOAA data (1*1 degree, ftp://arlftp.arlhq.noaa.gov/pub/archives/gdas1/)  
or 2.ERA5 data (higher resolution but need to convert the format)

## Steps
### 1. install HYSPLIT
just download the version that is suitable for your computer system from the website(https://www.ready.noaa.gov/HYSPLIT.php)

### 2. Data download
The data used must include all the time needed for the simulation.
If you want to find out where the rain came from, you need to know when it started and ended.
eg: the rainfall happened between 00:00 UTC on 21 July 2021 and 10:00 UTC on 22 July 2021. Simulate backward 10 days. Then the data must include the time period from 11 July 2021 at 00:00 UTC to 22 July 2021 at 10:00 UTC.

#### 2.1 
For NOAA data, .w1 means the first week of that month. To do the simulation in this example, you need to download W2 and W3.

#### 2.2
For ERA5 data, you can be more flexible with the time range, but you'll need 3D and 2D data to convert. So get data from the web site (https://cds.climate.copernicus.eu/datasets/reanalysis-era5-pressure-levels?tab=overview and https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview)
with these variable 

var2d ： ['Surface_pressure_surface','2_metre_temperature_surface','10_metre_U_wind_component_surface','10_metre_V_wind_component_surface','Boundary_layer_height_surface','Convective_available_potential_energy_surface','Instantaneous_eastward_turbulent_surface_stress_surface','Instantaneous_northward_turbulent_surface_stress_surface']

var3d ： ['Geopotential_isobaric','Temperature_isobaric','Vertical_velocity_isobaric','U_component_of_wind_isobaric','V_component_of_wind_isobaric','Relative_humidity_isobaric']
    
### 3. RUN HYSPLIT
#### 3.0 Set output meteorology variable
add parameters about humidity
![Uploading image.png…]()










