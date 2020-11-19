# Fishing Report Analysis
This is an analysis of the fisherman's report for Deep Sea Charter Boats in Southern California.

The Web Scraper extracts the website page's daily reports.
    The most it goes back is the 1st of the previous year

The Data Scrubber prepares the data for analysis, changing a string of multiple fish species and their catch numbers to columns and values respectively.

The Analysis focuses on larger game fish to find out which boat and/or trip type caught more large game fish per person.

## Adding weather data to practice Clustering and see if weather has a role to play
### Still working on this...

Added Standard Meteorological Data gathered from ocean buoys [here](https://www.ndbc.noaa.gov/)

Data Descriptions from https://www.ndbc.noaa.gov/:

#YY  MM DD hh mm WDIR WSPD GST  WVHT   DPD   APD MWD   PRES  ATMP  WTMP  DEWP  VIS PTDY
#yr  mo dy hr mn degT m/s  m/s     m   sec   sec degT   hPa  degC  degC  degC  nmi  hPa
2014 09 11 16 50 120  5.0  6.0   0.6     6   4.2 134 1016.5  29.3  30.5  24.4   MM +0.3

WDIR 	Wind direction (the direction the wind is coming from in degrees clockwise from true N) during the same period used for WSPD. See Wind Averaging Methods

WSPD 	Wind speed (m/s) averaged over an eight-minute period for buoys and a two-minute period for land stations. Reported Hourly. See Wind Averaging Methods.

GST 	Peak 5 or 8 second gust speed (m/s) measured during the eight-minute or two-minute period. The 5 or 8 second period can be determined by payload, See 
the Sensor Reporting, Sampling, and Accuracy section.

WVHT 	Significant wave height (meters) is calculated as the average of the highest one-third of all of the wave heights during the 20-minute sampling period. See the Wave Measurements section.

DPD 	Dominant wave period (seconds) is the period with the maximum wave energy. See the Wave Measurements section.

APD 	Average wave period (seconds) of all waves during the 20-minute period. See the Wave Measurements section.

MWD 	The direction from which the waves at the dominant period (DPD) are coming. The units are degrees from true North, increasing clockwise, with North as 0 (zero) degrees and East as 90 degrees. See the Wave Measurements section.

PRES 	Sea level pressure (hPa). For C-MAN sites and Great Lakes buoys, the recorded pressure is reduced to sea level using the method described in NWS Technical Procedures Bulletin 291 (11/14/80). ( labeled BAR in Historical files)

ATMP 	Air temperature (Celsius). For sensor heights on buoys, see Hull Descriptions. For sensor heights at C-MAN stations, see C-MAN Sensor Locations

WTMP 	Sea surface temperature (Celsius). For buoys the depth is referenced to the hull's waterline. For fixed platforms it varies with tide, but is referenced to, or near Mean Lower Low Water (MLLW).
DEWP 	Dewpoint temperature taken at the same height as the air temperature measurement.

VIS 	Station visibility (nautical miles). Note that buoy stations are limited to reports from 0 to 1.6 nmi.

PTDY 	Pressure Tendency is the direction (plus or minus) and the amount of pressure change (hPa)for a three hour period ending at the time of observation. (not in Historical files)

TIDE 	The water level in feet above or below Mean Lower Low Water (MLLW).
*Excluding TIDE since all values were 99/erroneous