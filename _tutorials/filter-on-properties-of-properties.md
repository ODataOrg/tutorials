---
name: Filter on properties of properties
categories: Filtering Collections
---

**Description**: You can use any related properties in a filter clause by using the same segments used in the path to traverse properties.

**Request**

```
GET http://services.odata.org/V4/TripPinService/Airports?$filter=Location/City/Region eq 'California'

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#Airports",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/Airports('KSFO')",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/Airports('KSFO')",
            "IcaoCode": "KSFO",
            "Name": "San Francisco International Airport",
            "IataCode": "SFO",
            "Location": {
                "Address": "South McDonnell Road, San Francisco, CA 94128",
                "City": {
                    "CountryRegion": "United States",
                    "Name": "San Francisco",
                    "Region": "California"
                },
                "Loc": {
                    "type": "Point",
                    "coordinates": [
                        -122.374722222222,
                        37.6188888888889
                    ],
                    "crs": {
                        "type": "name",
                        "properties": {
                            "name": "EPSG:4326"
                        }
                    }
                }
            }
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/Airports('KLAX')",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/Airports('KLAX')",
            "IcaoCode": "KLAX",
            "Name": "Los Angeles International Airport",
            "IataCode": "LAX",
            "Location": {
                "Address": "1 World Way, Los Angeles, CA, 90045",
                "City": {
                    "CountryRegion": "United States",
                    "Name": "Los Angeles",
                    "Region": "California"
                },
                "Loc": {
                    "type": "Point",
                    "coordinates": [
                        -118.408055555556,
                        33.9425
                    ],
                    "crs": {
                        "type": "name",
                        "properties": {
                            "name": "EPSG:4326"
                        }
                    }
                }
            }
        }
    ]
}
```