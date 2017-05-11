
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

### Current API Request Limitations and how to get over them

The UI and code are free to be redistributed, edited and added to according to the Apache 2.0 License. The current master branch (which is published on [github pages](https://ibm-ba-il.github.io/TWC_WeatherDataDownload/) ) is supposed to be light weight and a simple interface for interacting with the TWC API, hence it has the following limitations:

1. The API hooked to the the UI page will only work to retrieve ALL standard variables availaible from The Weather Channel API.  If you want to limit the number of fields being used, you will need to send the chosen fields as part of the URL. This can be done by adding the fields as a string and appending it to the URL when making the request. Optionally you can also create a checkbox UI to select certain fields and pass them into the URL. All code for the URL formation is in the index.html page. To learn more about field selection please look at [Weather Channel API Guide(Docs/TWC_CleanedObservations_API_Documentation.pdf).
2. Only Historical dates are expected. To get future forecasts please visit [The Weather Company](http://www.theweathercompany.com/) link and get information about APIS that can also send forecasted data for future dates.
3. No date validation check
4. Weather information for only a single location can be exported. 
5. Different sets of fields are exported for "Hourly" and "Daily" interval. To learn more about it, please look at the API documentation in the docs folder.
6. In the exported data, the time zone is set to GMT(by default), but can be changed by passing the desired time zone default as part of the url, code in index.html. 

## License
[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

## References
[The Weather Company](http://www.theweathercompany.com/)

[Historical Weather](https://docs.google.com/document/d/1asVeP3zFjSEYq_HXU4hpXgOcvz3jW1J2Z04guXCSZX0)

[IBM MarketPlace for Sales](https://www.ibm.com/us-en/marketplace/weather-company-data-packages)


## Contact/Authors
Vikremjeet singh bhagi (vsbhagi@us.ibm.com)
Ruth Briones (rbrione@us.ibm.com)
