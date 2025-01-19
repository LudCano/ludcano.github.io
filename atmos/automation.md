# Automation projects
These two projects are pretty similar, both use [Github Actions](https://github.com/features/actions) for generating plots and retrieving data from different sources.

## AOD Plotting
Check out the Github Repo  
[![LudCano/aod_plotting - GitHub](https://gh-card.dev/repos/LudCano/aod_plotting.svg)](https://github.com/LudCano/aod_plotting)

**<span style="color: green;">[Check this project running live](https://ludcano.github.io/aod_plotting/)</span>**

This project retrieves data for three places of interest: Mount Chacaltaya (GAW Station), Cota Cota Campus (LFA), and Santa Cruz (UTEPSA), these three locations have an [AERONET Instrument](https://aeronet.gsfc.nasa.gov) that measures AOD, to compare this with a satellite measurement, data from [GOES](https://www.star.nesdis.noaa.gov/goes/index.php) is retrieved and the pixel value for the stations is plotted too. This code runs (almost) 4 times each hour*.
All these plots must be saved in the same repository and the time series for future use.

Below an example:
![Example for this project running](images/example_aod_plotting.png)





* Github Actions lets you schedule the times for the code to run, nonetheless this is almost never accomplished, sometimes it can stop working for some hours or not follow the scheduled times.
