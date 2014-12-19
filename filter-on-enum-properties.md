Categories: Filtering collections

You can filter any type of collection in OData services. When referring to a member of enum properties, please don't ignore the namespace for the enum property.

Request

```
GET http://services.odata.org/V4/TripPinService/People?$filter=Gender eq Microsoft.OData.SampleService.Models.TripPin.PersonGender'Female'

Accept: application/json
OData-MaxVersion: 4.0
```

Response

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24filter=Gender+eq+Microsoft.OData.SampleService.Models.TripPin.PersonGender%27Female%27&%24skiptoken=8",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('elainestewart')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
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
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('salliesampson')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('salliesampson')",
            "UserName": "salliesampson",
            "FirstName": "Sallie",
            "LastName": "Sampson",
            "Emails": [
                "Sallie@example.com",
                "Sallie@contoso.com"
            ],
            "AddressInfo": [
                {
                    "Address": "87 Polk St. Suite 5",
                    "City": {
                        "CountryRegion": "United States",
                        "Name": "San Francisco",
                        "Region": "CA"
                    }
                },
                {
                    "Address": "89 Chiaroscuro Rd.",
                    "City": {
                        "CountryRegion": "United States",
                        "Name": "Portland",
                        "Region": "OR"
                    }
                }
            ],
            "Gender": "Female",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('jonirosales')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('jonirosales')",
            "UserName": "jonirosales",
            "FirstName": "Joni",
            "LastName": "Rosales",
            "Emails": [
                "Joni@example.com",
                "Joni@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('georginabarlow')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
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
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('angelhuffman')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('angelhuffman')",
            "UserName": "angelhuffman",
            "FirstName": "Angel",
            "LastName": "Huffman",
            "Emails": [
                "Angel@example.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('laurelosborn')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('laurelosborn')",
            "UserName": "laurelosborn",
            "FirstName": "Laurel",
            "LastName": "Osborn",
            "Emails": [
                "Laurel@example.com",
                "Laurel@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('sandyosborn')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('sandyosborn')",
            "UserName": "sandyosborn",
            "FirstName": "Sandy",
            "LastName": "Osborn",
            "Emails": [
                "Sandy@example.com",
                "Sandy@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635545679851504300
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ursulabright')",
            "@odata.etag": "W/\"08D1E96DB61542A3\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('ursulabright')",
            "UserName": "ursulabright",
            "FirstName": "Ursula",
            "LastName": "Bright",
            "Emails": [
                "Ursula@example.com",
                "Ursula@contoso.com"
            ],
            "AddressInfo": [],
            "Gender": "Female",
            "Concurrency": 635545679851504300
        }
    ]
}
```