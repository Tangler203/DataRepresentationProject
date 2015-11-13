
# County Galway Libraries API
## Data Representation and Querying Project 2015
### Liam Joyce

## Introduction
This project provides the design and documentation for the dataset "County Galway Libraries" which is available at [data.gov.ie](https://data.gov.ie/dataset/county-galway-libraries)

## About the Dataset
This dataset was received in Comma Separated Values (CSV) format, and was downloaded from [*here*]( http://data.galwaycoco.opendata.arcgis.com/datasets/eb71973a8a5b41d398fd0acc8613ea2a_0.csv ).
The CSV file contains 30 rows, the first being a header row with the names of each field, and 24 columns.
The Columns are as follows:

  - **X** : the x coordinate.
  - **Y** : the y coordinate.
  - **Council_ID**: the council ID.
  - **Administrative_Authority**: the controlling body.
  - **Name**: the name of the Library.
  - **Address1**: address of Library.
  - **Address2**: 2nd address of library, if applicable.
  - **Town**: the town of the library.
  - **Postcode**: library post code.
  - **County**: what county it is situated in.
  - **Services**: what services available at the library.
  - **Phone**: contact phone number.
  - **Email**: contact email address.
  - **Website** : website of library.
  - **Image**: image of library, if available.
  - **WGS84Latitude**: latitude of library.
  - **WGS84Longitude**: longitude of library.
  - **Opening_Hours_Monday**: the librarys opening hours on Monday.
  - **Opening_Hours_Tuesday**: the librarys opening hours on Tuesday.
  - **Opening_Hours_Wednesday**: the librarys opening hours on Wednesday.
  - **Opening_Hours_Thursday**: the librarys opening hours on Thursday.
  - **Opening_Hours_Friday**: the librarys opening hours on Friday.
  - **Saturday**: the librarys opening hours on Saturday.
  - **OBJECTID**: unique object ID.
    
    
    
    ## Get library by ID
    You can get a library with its unique object ID using the GET method at the following URL:
    *http://galwaylibraries.com/id/[OBJECTID]*
    where you replace [OBJECTID] with the object ID.
    For example, the URL:
    *http://galwaylibraries.com/id/1*
    will return the library with object ID '1'.
    The data will be returned with the following data in: 
    
    ```json
    [
        {
        "X":-9.07446057544246,
        "Y":53.277400205441175,
        "Council_ID":"GY",
        "Administrative_Authority":"GALWAY COUNTY COUNCIL",
        "Name":"WESTSIDE LIBRARY",
        "Address1":"SEAMUS QUIRKE ROAD",
        "Address2":"",
        "Town":"GALWAY City",
        "Postcode":000000,
        "County":"COUNTY GALWAY",
        "Services":"",
        "Phone":+353 (0) 91 520616,
        "Email":"westside@gaOpening_Hours_Monday lwaylibrary.ie",
        "Website":"http://www.galway.ie/en/Services/Library/",
        "Image":"",
        "WGS84Latitude":53.27739,
        "WGS84Longitude2:-9.07447,
        "Opening_Hours_Monday":"Closed",
        "Opening_Hours_Tuesday":"11.00am to 8.00pm",
        "Opening_Hours_Wednesday":"1.00am to 8.00pm",
        "Opening_Hours_Thursday":"11.00am to 5.00pm",
        "Opening_Hours_Friday":"11.00am to 5.00pm",
        "Opening_Hours_Saturday":"11.00am to 1.00pm and 2.00pm to 5.00pm",
        "OBJECTID":1
        }
    ]
    ```
    
    
    ## Get library by Town
    You can get a list of libraries in a town using the GET method at the following URL:
    *http://galwaylibraries.com/town/[TOWN]*
    where you replace [TOWN] with the town.
    For example, the URL:
    *http://galwaylibraries.com/town/Galway City*
    will return the library with the town of 'Galway City'.
    The data will be returned with the following data in: 
    
    ```json
    [
        {
        "X":-9.07446057544246,
        "Y":53.277400205441175,
        "Council_ID":"GY",
        "Administrative_Authority":"GALWAY COUNTY COUNCIL",
        "Name":"WESTSIDE LIBRARY",
        "Address1":"SEAMUS QUIRKE ROAD",
        "Address2":"",
        "Town":"GALWAY City",
        "Postcode":000000,
        "County":"COUNTY GALWAY",
        "Services":"",
        "Phone":+353 (0) 91 520616,
        "Email":"westside@galwaylibrary.ie",
        "Website":"http://www.galway.ie/en/Services/Library/",
        "Image":"",
        "WGS84Latitude":53.27739,
        "WGS84Longitude2:-9.07447,
        "Opening_Hours_Monday":"Closed",
        "Opening_Hours_Tuesday":"11.00am to 8.00pm",
        "Opening_Hours_Wednesday":"1.00am to 8.00pm",
        "Opening_Hours_Thursday":"11.00am to 5.00pm",
        "Opening_Hours_Friday":"11.00am to 5.00pm",
        "Opening_Hours_Saturday":"11.00am to 1.00pm and 2.00pm to 5.00pm",
        "OBJECTID":1
        }
        
        {
        "X":-9.002184575683327,
        "Y":53.282740990239205,
        "Council_ID":"GY",
        "Administrative_Authority":"GALWAY COUNTY COUNCIL",
        "Name":"BALLYBANE PUBLIC LIBRARY",
        "Address1":"BALLYBANE NEIGHBOURHOOD VILLAGE",
        "Address2":"CASTLEPARK ROAD",
        "Town":"GALWAY City",
        "Postcode":000000,
        "County":"COUNTY GALWAY",
        "Services":"",
        "Phone":+353 (0) 91 380590,
        "Email":"ballybane@galwaylibrary.ie",
        "Website":"http://www.galway.ie/en/Services/Library/",
        "Image":"",
        "WGS84Latitude":53.282731,
        "WGS84Longitude2:-9.002194,
        "Opening_Hours_Monday":"Closed",
        "Opening_Hours_Tuesday":"11:00 to 13:00 and 14:00 to 17:00",
        "Opening_Hours_Wednesday":"11:00 to 13:00 and 14:00 to 17:00",
        "Opening_Hours_Thursday":"11:00 to 13:00 and 14:00 to 17:00",
        "Opening_Hours_Friday":"11:00 to 13:00 and 14:00 to 17:00",
        "Opening_Hours_Saturday":"11:00 to 13:00 and 14:00 to 17:00",
        "OBJECTID":8
        }
        
        {
        "X":-9.052011015315966,
        "Y":53.271532932942051,
        "Council_ID":"GY",
        "Administrative_Authority":"GALWAY COUNTY COUNCIL",
        "Name":"Galway City Library",
        "Address1":"HYNES BUILDINGS",
        "Address2":"HYNES BUILDINGS",
        "Town":"GALWAY City",
        "Postcode":000000,
        "County":"COUNTY GALWAY",
        "Services":"",
        "Phone":+353 (0) 91 561666,
        "Email":"info@galwaylibrary.ie",
        "Website":"http://www.galway.ie/en/Services/Library/",
        "Image":"",
        "WGS84Latitude":0,
        "WGS84Longitude2:0,
        "Opening_Hours_Monday":"2.00pm to 5.00pm",
        "Opening_Hours_Tuesday":"11.00am to 8.00pm",
        "Opening_Hours_Wednesday":"11.00am to 8.00pm",
        "Opening_Hours_Thursday":"11.00am to 8.00pm",
        "Opening_Hours_Friday":"11.00am to 5.00pm",
        "Opening_Hours_Saturday":"11.00am to 5.00pm",
        "OBJECTID":29
        }
    ]
    ```


    
