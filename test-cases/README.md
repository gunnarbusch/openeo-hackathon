# Test Cases
To get a first insight in the setup and use of openEO, we start with some test cases. The test cases are mostly covering the basic functionality of the client libraries ([Python](https://github.com/Open-EO/openeo-python-client), [R](https://github.com/Open-EO/openeo-r-client)) and the [API](https://github.com/Open-EO/openeo-api). You can work on the test cases with the their own computers and with your preferred IDE/Editor.

We are using two back-ends to perform these tasks:

* [openEO GeoPyspark back-end](https://github.com/Open-EO/openeo-geopyspark-driver)
  * URL: http://openeo.vgt.vito.be/openeo
  * Credentials: none
* [openEO Google Earth Engine back-end](https://github.com/Open-EO/openeo-earthengine-driver)
  * URL: http://giv-project8.uni-muenster.de
  * Credentials: Username is `groupX`  with X being the group number and password `test123`

## Task 1

Please install one of the openEO clients. Make sure that the client is properly working by connecting to one the back-ends and requesting the capabilities that are provided by the back-end.

## Task 2

You want to know which products and processes are offered by the back-end. Please find this information. Furthermore, you want to know which temporal extent is available for a specific product (e.g. Sentinel-2) and which arguments need to be provided for the `ndvi ` process.

## Task 3

You want to derive minimum NDVI measurements over pixel time series of Sentinel-2 data of Vienna. The extends that you are interested in:

* bounding box (left: 16.138916, top: 48.320647, right: 16.524124, bottom: 48.138600, EPSG:4326)
* temporal extent (01.01.2018 – 31.01.2018)

You want to download the results as PNG (with additional color stretching) or GeoTiff.

## Task 4

*In this task you'll use the Python client and the openEO GeoPyspark back-end only.*

First of all, you want to find out which Sentinel-2 data is available at the back-end, as well as if the back-end provides User-Defined-Functions (UDFs). You want to run the provided Python script on each time series of the dataset. The extents are defined by: 

* bounding box (left: 16.138916, top: 48.320647, right: 16.524124, bottom: 48.138600, EPSG:4326)
* temporal extent (01.01.2018 – 31.01.2018)

You want to download the results as GeoTiff.

## Task 5

You want to compute time series of zonal statistics (arithmetic mean / average) of Sentinel-2 data using a predefined polygon. First of all you should check if zonal-statistics is provided by the back-end. Furthermore you need to upload [the prepared polygon](task-5/polygon.json). Use the following extents and band: 

* bounding box (left: 16.138916, top: 48.320647, right: 16.524124, bottom: 48.138600, EPSG:4326)
* temporal extent (01.01.2018 – 31.01.2018)
* band 8

You want to perform a batch processing and afterwards download the results as JSON.

## Solutions

* [Task 1](task-1/solution.md)
* [Task 2](task-2/solution.md)
* [Task 3](task-3/solution.md)
* [Task 4](task-4/solution.md)
* [Task 5](task-5/solution.md)