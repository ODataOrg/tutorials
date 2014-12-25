**Categories**: Operations

**Description**: OData support unbound custom functions. The unbound functions can be invoked either with parameters or not and unbound functions can be viewed in the $metadata. Note: OData functions CANNOT have side effect, so only GET verb is allowed.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/GetNearestAirport(lat = 33, lon = -118)

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#Airports/$entity",
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
```

