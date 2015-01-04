---
name: Format
categories: Other System Query Options
---

**Description**: By default OData services return an extremely compact JSON format. This happens by stripping out all of the metadata that should be calculable by "smart" OData clients. For generic hypermedia clients, you can request additional metadata by using the Accept header or $format system query option to request application/json;odata.metadata=full. In this case, we get a bunch of additional annotations in the payload indicating type information and relationships to related resources.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/People?$format=application/json;odata.metadata=full

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24format=application%2fjson%3bodata.metadata%3dfull&%24skiptoken=8",
    "value": [
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
            "UserName": "russellwhyte",
            "FirstName": "Russell",
            "LastName": "Whyte",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Russell@example.com",
                "Russell@contoso.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [
                {
                    "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Location",
                    "Address": "187 Suffolk Ln.",
                    "City": {
                        "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.City",
                        "CountryRegion": "United States",
                        "Name": "Boise",
                        "Region": "ID"
                    }
                }
            ],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('russellwhyte')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "UserName": "scottketchum",
            "FirstName": "Scott",
            "LastName": "Ketchum",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Scott@example.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [
                {
                    "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Location",
                    "Address": "2817 Milton Dr.",
                    "City": {
                        "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.City",
                        "CountryRegion": "United States",
                        "Name": "Albuquerque",
                        "Region": "NM"
                    }
                }
            ],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('scottketchum')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')",
            "UserName": "ronaldmundy",
            "FirstName": "Ronald",
            "LastName": "Mundy",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Ronald@example.com",
                "Ronald@contoso.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('ronaldmundy')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')",
            "UserName": "javieralfred",
            "FirstName": "Javier",
            "LastName": "Alfred",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Javier@example.com",
                "Javier@contoso.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [
                {
                    "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Location",
                    "Address": "89 Jefferson Way Suite 2",
                    "City": {
                        "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.City",
                        "CountryRegion": "United States",
                        "Name": "Portland",
                        "Region": "WA"
                    }
                }
            ],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('javieralfred')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "UserName": "willieashmore",
            "FirstName": "Willie",
            "LastName": "Ashmore",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Willie@example.com",
                "Willie@contoso.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('willieashmore')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')",
            "UserName": "vincentcalabrese",
            "FirstName": "Vincent",
            "LastName": "Calabrese",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Vincent@example.com",
                "Vincent@contoso.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [
                {
                    "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Location",
                    "Address": "55 Grizzly Peak Rd.",
                    "City": {
                        "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.City",
                        "CountryRegion": "United States",
                        "Name": "Butte",
                        "Region": "MT"
                    }
                }
            ],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('vincentcalabrese')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "UserName": "clydeguess",
            "FirstName": "Clyde",
            "LastName": "Guess",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Clyde@example.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('clydeguess')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        },
        {
            "@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.Person",
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "UserName": "keithpinckney",
            "FirstName": "Keith",
            "LastName": "Pinckney",
            "Emails@odata.type": "#Collection(String)",
            "Emails": [
                "Keith@example.com",
                "Keith@contoso.com"
            ],
            "AddressInfo@odata.type": "#Collection(Microsoft.OData.SampleService.Models.TripPin.Location)",
            "AddressInfo": [],
            "Gender@odata.type": "#Microsoft.OData.SampleService.Models.TripPin.PersonGender",
            "Gender": "Male",
            "Concurrency@odata.type": "#Int64",
            "Concurrency": 635550870519871400,
            "Friends@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Friends/$ref",
            "Friends@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Friends",
            "Trips@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Trips/$ref",
            "Trips@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Trips",
            "Photo@odata.associationLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Photo/$ref",
            "Photo@odata.navigationLink": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Photo",
            "#Microsoft.OData.SampleService.Models.TripPin.ShareTrip": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.ShareTrip",
                "target": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline",
                "target": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline"
            },
            "#Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips": {
                "title": "Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips",
                "target": "http://services.odata.org/V4/TripPinService/People('keithpinckney')/Microsoft.OData.SampleService.Models.TripPin.GetFriendsTrips"
            }
        }
    ]
}
```

