---
name: Top / Skip
categories: Other System Query Options
---

**Description**: There are two types of paging in OData services. Servers can enable server-side paging, returning nextLinks that clients can follow to subsequent pages. Clients can drive paging using $top and $skip.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/People?$top=2&$skip=2

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
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
        }
    ]
}
```

