# Obtain data from APIs

Often we can retrieve data using a SQL query of by downloading a CSV file.  But often websites provide APIs (Application Programming Interfaces) that allow us to retieve data programmatically.  These provide us a way to connect over the web, specify what we want and recieve the data we specify.  Working with complex APIs or automating the communicaton requires programming in a language such as Python or Javascript.  But for straight forward APIs we can the retrieve what we want with a tool such as Postman or Curl.  In this lesson we will learn how to retrieve the data we want for websites and then convert it for use with Excel and Tableau.

### Lesson objectives
*By the end of this lesson, you will be able to:*
* Retrieve data from a simple API with Postman
* Evaluate the JSON files returned by using JSON viewing tools and JSON to CSV converters
* Import JSON data retrieved from the APIs into Tableau


### Pre-work
* Download and install the [Postman app](https://www.getpostman.com/)
* Read this short introductory article on APIs and JSON format:
  * [Web APIs for non-programmers](https://schoolofdata.org/2013/11/18/web-apis-for-non-programmers/)]
* Read this short introductory article on the JSON data interchange format
  * [What is JSON? JavaScript Object Notation explained](https://www.infoworld.com/article/3222851/javascript/what-is-json-javascript-object-notation-explained.html)

### Fetch data through APIs

**Discuss APIs  -  15 min**
* [Slides](https://docs.google.com/presentation/d/1mYOwpgXKaQly3RL-r0N8LAEMdLKXTXA8fRrq6JTCvQ8/edit?usp=sharing)
* Discuss these topics
  * If a site enables programmatic retrieval they typically do it though APIs
  * Anatomy of an API call
  * Data returned will be formatted as text, typically JSON but sometimes XML format
  * APIs vs web scraping
* Take a look at a list of public APIs at [public-apis.io](https://public-apis.io/)

**Code Along   Retrieve data through an API with Postman  -  20 min**
* Discuss Postman and curl as two ways to interactively retrieve data
  * curl is a powerful command line capability that can conceivably imitate any request over the web
  * Postman is a more recent tool with an interactive UI for creating and delivering requests to an API and retrieving the results  
* Some site APIs are complex enough that they benefit from using a computer language and some supporting libraries
  * Ex.  Python + a site's API package
  * In those cases, Postman or curl will not be sufficient to retrieve all possible data from a site through it's
  * But for simpler API's, Postman and curl retrieve what you need
* Tour the Postman interface
* Create an API request (call) in Postman
  * Use the [Open Movie Database  (ODBM)](http://www.omdbapi.com/) website API
  * Review documentation of the API on page
  * Build some API calls using the interactive API call builder on the site
  * Obtain user key is you don't have one using the menu at the top of the page
  * Create an API call in Postman
* Submit the API call to a website and retrieve data
* Examine data in a simple text browser such as Notepad (Windows) or TextEdit (Mac)
* Examine data after viewing in a JSON format
  * Use a format tool on a web page or use a local tool such as JSON formatters for Chrome

#### Investigate other APIs For further exploration the [Apple Music API](https://developer.apple.com/documentation/applemusicapi) are good ones to investigate.

**Exercise   Retrieve data from a website with an API  -  20 min**
* You have been asked to provide analysis of US exports over the past few years of years 2016.  Specifically you need to analyze data from 2016-2018.  You have found a good source of data on the Census Bureau's web site.  The site makes the data available through an API.
  * [The API documentation](https://www.census.gov/foreign-trade/reference/guides/Guide%20to%20International%20Trade%20Datasets.pdf)
  * [Census Bureau trade data](https://www.census.gov/data/developers/data-sets/international-trade.html)
* Work in pairs
* Use Postman to retrieve the data from the API
 * Create an API call (request) in Postman that will retrieve the data
   * Tip: You can retrieve a whole year at a time but is not obvious how to do it since the documentation example implies month needs to be added when specifying the time range for the data
 * Send the API call to a website and retrieve the data
* Examine data in a simple text browser such as Notepad or TextEdit
* Create a data source in Tableau that UNION ALLs the retrieved files into one data source for 2016-2018
* Save your Tableau Public workbook
<br>

**Break  -  5 min**

### Find information in the JSON files returned

**Discuss Use JSON viewing and conversion tools  -  20 min**
* JSON viewing tool
  * Demonstrate several formatters/viewers on the web
  * Show options available for download
    * [MiTec JSON Viewer](https://www.mitec.cz/jsonv.html) (Windows)
    * [Web JSON viewer](https://codebeautify.org/jsonviewer)
* JSON to CSV converter options
  * Web
  * Local

**Code along   View the JSON returned  -  20 min**
* Reveal the structure of the JSON
* Find specific values for a unique ID

**Code along   Convert JSON to CSV files  -  10 min**
* Use a converter on the Web
* Use a local converter

**Code along   Import JSON into Tableau  -  15 min**
* Convert JSON to CSV
* In Tableau, read the JSON file as a data source
  * Note that Tableau will have trouble reading some JSON correctly even though some converters will convert the same Jason to CSV without a problem
* In Tableau, read the CSV file as a data source
* Blend the two data sources (remember to link all dimensions possible)
* Create a report comparing the two data sources


### Resources
