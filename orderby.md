**Categories**: Other system query options

**Description**: You can use the \$orderby system query option to specify ordering criteria. You can use many of the functions usable in $filter in $orderby as well.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/People?$orderby=length(FirstName) desc,UserName

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24orderby=length(FirstName)+desc%2cUserName&%24skiptoken=8",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('genevievereeves')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('genevievereeves')",
            "UserName": "genevievereeves",
            "FirstName": "Genevieve",
            "LastName": "Reeves",
            "Emails": [
                "Genevieve@example.com",
                "Genevieve@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('georginabarlow')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('georginabarlow')",
            "UserName": "georginabarlow",
            "FirstName": "Georgina",
            "LastName": "Barlow",
            "Emails": [
                "Georgina@example.com",
                "Georgina@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('marshallgaray')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('elainestewart')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('elainestewart')",
            "UserName": "elainestewart",
            "FirstName": "Elaine",
            "LastName": "Stewart",
            "Emails": [
                "Elaine@example.com",
                "Elaine@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('kristakemp')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('kristakemp')",
            "UserName": "kristakemp",
            "FirstName": "Krista",
            "LastName": "Kemp",
            "Emails": [
                "Krista@example.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635550870519871400
        }
    ]
}
```

