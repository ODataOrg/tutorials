---
name: Any/All filter
categories: Filtering Collections
---

**Description**: You can use any/all lambda-style filters for collection properties.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People?$filter=Emails/any(e: endswith(e, 'contoso.com'))

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24filter=Emails%2fany(e%3a+endswith(e%2c+%27contoso.com%27))&%24skiptoken=8",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "UserName": "russellwhyte",
            "FirstName": "Russell",
            "LastName": "Whyte",
            "Emails": [
                "Russell@example.com",
                "Russell@contoso.com"
            ],
            "AddressInfo": [
                {
                    "Address": "187 Suffolk Ln.",
                    "City": {
                        "CountryRegion": "United States",
                        "Name": "Boise",
                        "Region": "ID"
                    }
                }
            ],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "UserName": "ronaldmundy",
            "FirstName": "Ronald",
            "LastName": "Mundy",
            "Emails": [
                "Ronald@example.com",
                "Ronald@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "UserName": "javieralfred",
            "FirstName": "Javier",
            "LastName": "Alfred",
            "Emails": [
                "Javier@example.com",
                "Javier@contoso.com"
            ],
            "AddressInfo": [
                {
                    "Address": "89 Jefferson Way Suite 2",
                    "City": {
                        "CountryRegion": "United States",
                        "Name": "Portland",
                        "Region": "WA"
                    }
                }
            ],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "UserName": "willieashmore",
            "FirstName": "Willie",
            "LastName": "Ashmore",
            "Emails": [
                "Willie@example.com",
                "Willie@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        },
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
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "UserName": "keithpinckney",
            "FirstName": "Keith",
            "LastName": "Pinckney",
            "Emails": [
                "Keith@example.com",
                "Keith@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('marshallgaray')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('marshallgaray')",
            "UserName": "marshallgaray",
            "FirstName": "Marshall",
            "LastName": "Garay",
            "Emails": [
                "Marshall@example.com",
                "Marshall@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ryantheriault')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('ryantheriault')",
            "UserName": "ryantheriault",
            "FirstName": "Ryan",
            "LastName": "Theriault",
            "Emails": [
                "Ryan@example.com",
                "Ryan@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635545679851504300
        }
    ]
}
```