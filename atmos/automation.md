# Automation projects

[Back to Atmospheric Physics Projects](../atmosindex)

These three projects are pretty similar, all of them use [Github Actions](https://github.com/features/actions) for generating plots and retrieving data from different sources. The advantages of using this tool are: 1) We don't have to have a computer running all the time. 2. Compared to downloading into a local file, downloading data from the cloud to the cloud (in this case the Github repo) is way quicker. And 3. It's free! (with limits).

---
## AOD Plotting
In 2023 and 2024, Bolivia saw an important increase in wildfires[^1], for several days, cities even in the Andes a decrease in air quality, this tool was developed for monitoring the AOD for Bolivia (closely related to emissions from the burning season).

Check out the Github Repo  
[![LudCano/aod_plotting - GitHub](https://gh-card.dev/repos/LudCano/aod_plotting.svg)](https://github.com/LudCano/aod_plotting)

**<span style="color: green;">[Check this project running live](https://ludcano.github.io/aod_plotting/)</span>**

This project retrieves data for three places of interest: Mount Chacaltaya (GAW Station), Cota Cota Campus (LFA), and Santa Cruz (UTEPSA), these three locations have an [AERONET Instrument](https://aeronet.gsfc.nasa.gov) that measures AOD, to compare this with a satellite measurement, data from [GOES](https://www.star.nesdis.noaa.gov/goes/index.php) is retrieved and the pixel value for the stations is plotted too. This code runs (almost) 4 times each hour[^2].
All these plots must be saved in the same repository and the time series for future use.

Below an example:
![Example for this project running](images/example_aod_plotting.png)

---
## Pluviometry Plotting
Check out the Github Repo  
[![LudCano/pluvio-plots - GitHub](https://gh-card.dev/repos/LudCano/pluvio-plots.svg)](https://github.com/LudCano/pluvio-plots)

**<span style="color: green;">[Check this project running live]([https://ludcano.github.io/aod_plotting/](https://github.com/LudCano/pluvio-plots/blob/main/plot_all_cotacota.png?raw=true))</span>**

La Paz is a complicated city, it was built practically above more than 300 rivers. The consequence? In the rainfall season, the bigger rivers become a problem. Also,the  effects of El Niño and Niña in the precipitation per year is still a topic to be fully understood, this small tool retrieves data from two Davis Stations (Campus Cota Cota and on the way to Chacaltaya) and plots the cumulative rainfall and some other event-related plots. This code also runs automatically 3 times per hour [^2].

This project is intended to grow, probably we can retrieve data from cities that don't have professional weather stations using airports' reports? Contact me if you have suggestions! :sweat_smile:

The plot generated:

![Example of plot](images/pluvio_example.png)


---
## UV Index Plotting
Check out the Github Repo  
[![LudCano/inti_uv - GitHub](https://gh-card.dev/repos/LudCano/inti_uv.svg)](https://github.com/LudCano/inti_uv)

**<span style="color: green;">[Check this project running live](https://sites.google.com/chacaltaya.edu.bo/iuv)</span>**


La Paz again! At an altitude of approximately 3,600 meters above sea level, we face challenges with UV radiation (check out [this interview](https://la-razon.com/lr-article/rayos-ultravioleta-llegan-a-un-indice-critico-en-la-paz/) with a researcher from the lab (in Spanish)), as the UV index can exceed 15. In such cases, it’s crucial for the public to take precautions and follow recommended guidelines[^3]. This code retrieves UV index data from an API provided by the lab technician and generates a user-friendly UV plot. While this page isn’t designed for scientific purposes, it serves as an outreach tool to raise awareness. This code also runs automatically 4 times per hour [^2].

This project is intended to grow, probably using satellite images and generate the same plot for different cities?. Contact me if you have suggestions! :sweat_smile:

The plot generated:

![Example of plot](images/inti_example.png)

---
[^1]: Read the [Copernicus Atmosphere Monitoring Service report on wildfires](https://atmosphere.copernicus.eu/cams-global-wildfires-review-2024-harsh-year-americas)
[^2]: Github Actions lets you schedule the times for the code to run, nonetheless this is almost never accomplished, sometimes it can stop working for some hours or not follow the scheduled times.
[^3]: For more information a good book for reference is [Radiación Ultravioleta en Bolivia (Spanish)](https://iris.paho.org/handle/10665.2/31072)
