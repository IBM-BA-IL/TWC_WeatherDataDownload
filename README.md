
# Simple HTML user interface for IBM Weather Company Data API

This project will allow users to download weather data using a simple user interface that uses The Weather Company APIs to download weather data. The downloaded data throught your web browser will be availaible in csv format(can be changed by forking and editing code). 

The user interface  for downloading the weather data can be found here : https://ibm-ba-il.github.io/TWC_WeatherDataDownload/
Please see the usage guide below for more details on existing functionality and ways to extend it.

## Usage

### Using the HTML UI
The current html UI: https://ibm-ba-il.github.io/TWC_WeatherDataDownload/ allows the user to download historical data for a location given a certain date range. 

UI Screenshot(Image): 
![](Docs/UIScreenshot.png?raw=true "UI Screenshot")

The data is downloaded in CSV and can be on a daily or hourly level.

Example Daily(Image): 
![](Docs/DailyExample.png?raw=true "Daily Example Data")

To download data from the UI you will need:

1. A valid API Key for The Weather Channel Data Packages. Contact : https://www.ibm.com/us-en/marketplace/weather-company-data-packages
2. Provide the form with a valid location. Please note Zipcode works only for US, lattitude and longitude work for all places. Use the dropdown to choose location input method.
3. Provide a date range. Dates can only be historical, and the "From Date" should be before the "To Date"
4. Time Interval can be "Hourly" or "Daily" which will determine what level the weather data is downloaded for. See Hourly and Daily examples above
5. Weather variables can be shown using either "Metric" or "Imperial" units. 

Please be adviced:

1. The API used for the UI page will only work to retrieve ALL standard variables availaible from The Weather Channel API. To learn about the variables exported see this : [Weather Channel API Guide](Docs/TWC Cleaned Observations API Documentation.pdf)



