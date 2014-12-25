**Categories**: Other system query options

**Description**: You can use the \$select system query option to only return specified properties.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/People?$select=FirstName,LastName

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People(FirstName,LastName)",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24select=FirstName%2cLastName&%24skiptoken=8",
    "value": [
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "FirstName": "Russell",
            "LastName": "Whyte"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "FirstName": "Scott",
            "LastName": "Ketchum"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "FirstName": "Ronald",
            "LastName": "Mundy"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "FirstName": "Javier",
            "LastName": "Alfred"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "FirstName": "Willie",
            "LastName": "Ashmore"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "FirstName": "Vincent",
            "LastName": "Calabrese"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "FirstName": "Clyde",
            "LastName": "Guess"
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "FirstName": "Keith",
            "LastName": "Pinckney"
        }
    ]
}
```

