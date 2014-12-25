**Categories**: Basic Requests

**Description**: One of the most common responses from a REST API is a collection of resources. In this case we asked for the People collection. For each response, the OData service writes a self-described response (another REST principle) by annotating the response with a context URL. This context URL tells the service that the contents of the response are a collection of things in the People entity set. The @odata.nextLink annotation is present because the server opted to split the result set across multiple pages. The client can also drive paging using $top and $skip, but server-side paging is a mitigation against DoS attacks. The value property contains the bulk of the response. Note that @odata.id and @odata.editLink should generally not be present in the payload unless they deviate from convention. In this case it appears that there is a bug in our sample service. Pretend those properties aren't there.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People

Accept: application/json
OData-MaxVersion: 4.0

```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24skiptoken=8",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
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
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "UserName": "scottketchum",
            "FirstName": "Scott",
            "LastName": "Ketchum",
            "Emails": [
                "Scott@example.com"
            ],
            "AddressInfo": [
                {
                    "Address": "2817 Milton Dr.",
                    "City": {
                        "CountryRegion": "United States",
                        "Name": "Albuquerque",
                        "Region": "NM"
                    }
                }
            ],
            "Gender": "Male",
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
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
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
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
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
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
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
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
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "UserName": "clydeguess",
            "FirstName": "Clyde",
            "LastName": "Guess",
            "Emails": [
                "Clyde@example.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635545521745890000
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "@odata.etag": "W/\"08D1E948E6410AFC\"",
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
            "Concurrency": 635545521745890000
        }
    ]
}
```