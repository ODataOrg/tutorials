**Categories**: Filtering collections

**Description**: The $filter system query option can be used to filter any collection of resources. Note that the response to a filtered collection is a collection of the same type, regardless of the number of matched resources.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People?$filter=FirstName eq 'Vincent'


Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "UserName": "vincentcalabrese",
            "FirstName": "Vincent",
            "LastName": "Calabrese",
            "Emails": [
                "Vincent@example.com",
                "Vincent@contoso.com"
            ],
            "AddressInfo": [
                {
                    "Address": "55 Grizzly Peak Rd.",
                    "City": {
                        "CountryRegion": "United States",
                        "Name": "Butte",
                        "Region": "MT"
                    }
                }
            ],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        }
    ]
}
```