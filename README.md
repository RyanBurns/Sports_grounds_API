## Data representation and querying project
#Ryan Burns - G00296445
My API to be used with a public sports grounds dataset in Galway
May be found at *https://data.gov.ie/dataset/galway-city-public-sports-facilities*

The Public Sports grounds in Galway City dataset contains information about all of the sports facilities around the city.
Information such as the parks name, location, opening hours, type of grounds: Rugby/Football/G.A.A.
This dataset could be used well with a mobile app, for users looking to find the closest public facilities.

## Galway City Public Sports Facilities

This dataset is of .CSV file type, and was downloaded from  https://data.gov.ie/dataset/galway-city-public-sports-facilities

The CSV file contains 48 rows, there are 12 columns with the following headings


| Heading       | Information          |
| ------------- |:-------------:| 
| X      | Longitude of the sports facility to 13 decimal places     | 
| Y      | Latitude of the sports facility to 13 decimal places      | 
| OBJECTID    | A numerical id for the sports facility       |   
| NUMBER      | Sports facility number      |
| TYPE      | G.AA/ Rugby/ Football     | 
| NAME      | Name of Sports Facilty      | 
| Lat     | Latitude of sports facility     | 
| Long      | Longitude of sports facility      | 
| EastITM     |Irish Transverse Mercator (ITM) East value      |
| NorthITM      | Irish Transverse Mercator (ITM) North vaule      |
| EastIG      | East Irish Grid Reference number      | 
| NorthIG     | North Irish Grid Reference number     |

## List of Rugby Grounds in Galway City
You can get a list of Rugby grounds in Galway City using the GET method at the following URL:
*http://galwaysportsfacilitiesapi.com/sports/[all]*

##Using the Datset
#Return all rugby facilities

Using the HTTP POST method, you can display a list of all the facilities/sports grounds in Galway City:
*http://galwaysportsfacilitiesapi.com/sports/[all]*

The data will be returned in JSON format,  here is the first line of the file in JSON format, this should illustrate how the data is displayed:

```javascript
[
  {
    "X": -9.13415204770846,
    "Y": 53.2644153571333,
    "OBJECTID":" 1",
    "NUMBER":" a01",
    "TYPE":" G.A.A Pitch",
    "NAME":" Cappagh Park",
    "Lat":" 53.264",
    "Long":" -9.134",
    "EastITM": 524337.139,
    "NorthITM": 724385.826,
    "EastIG": 124370.044,
    "NorthIG": 224356.434
  },
  { ... },
  { ... }
]
```

#Getting A List of Sports Facilities Nearby

You want to get the users location data and search for sports facilities close to them. You use the longitude and latitude, with a POST method, using the following URL:

http://galwaysportsfacilitiesapi.com/sports/closest-long-lat/

This will display all of the sports facilities, begining with the sportsground that is closest to the longitude and latitude coordinates provided.

to filter results returned by the POST method. This can be done using the following URL:

http://galwaysportsfacilitiesapi.com/sports/nearby-long-lat/[number]

Replace [number] with the number of sports grounds you want to be given back. This again will display all sports facilities nearby except this time it will only return the desired amount, and will list them in order of proximity.

Limiting the number of results returned back would look like this:

http://galwaysportsfacilitiesapi.com/sports/nearby-long-lat/3

This returns the 6 closest parks to the longitude and latitude used in the POST method.

##Conclusion
This API would be useful if somebody made an application for sports people around Galway, my imagined user is somebody who wants to know which sportsgrounds are open to public use, and what facilities are there : G.A.A / Soccer / Both.


