## Data representation and querying project
#Ryan Burns - G00296445
My API to be used with a public sports grounds dataset in Galway
May be found at [*https://data.gov.ie/data*]{*https://data.gov.ie/dataset/galway-city-public-sports-facilities*}

The Public Sports grounds in Galway City dataset contains information about all of the sports facilities around the city.
Information such as the parks name, location, opening hours, type of grounds: Rugby/Football/G.A.A.
This dataset could be used well with a mobile app, for users looking to find the closest public facilities.

## Galway City Public Sports Facilities

This dataset is of .CSV file type, and was downloaded from  https://data.gov.ie/dataset/galway-city-public-sports-facilities

The CSV file contains 48 rows, there are 12 columns with the following headings


| Heading       | Information          |
| ------------- |:-------------:| 
| X      | X Co-ordinate of the sports facility     | 
| Y      | Y Co-ordinate of the sports facility      | 
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
*http://galwaysportsfacilitiesapi.com/rugby/[all]*

Using the HTTP POST method, you can display a list of all the rugby facilities/sports grounds in Galway City:
*http://galwaysportsfacilitiesapi.com/rugby/[all]*

The data will be returned in JSON format,  here is the first line of the file in JSON format, this should illustrate how the data is displayed:

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
