**Categories**: Other system query options

**Description**: You can use the $expand system query option to include related resources. The expand clause can include many of the other system query options, enabling left-join type semantics. Also, you can expand <property>/$ref in order to get just the links to the related resources.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/People?$expand=Friends,Trips

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People",
    "@odata.nextLink": "http://services.odata.org/V4/TripPinService/People?%24expand=Friends%2cTrips&%24skiptoken=8",
    "value": [
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
            "Concurrency": 635550870519871400,
            "Friends": [
                {
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
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
                    "Concurrency": 635550870519871400
                },
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
                },
                {
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('angelhuffman')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
                    "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('angelhuffman')",
                    "UserName": "angelhuffman",
                    "FirstName": "Angel",
                    "LastName": "Huffman",
                    "Emails": [
                        "Angel@example.com"
                    ],
                    "AddressInfo": [],
                    "Gender": "Female",
                    "Concurrency": 635550870519871400
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('russellwhyte')/Trips",
            "Trips": [
                {
                    "TripId": 0,
                    "ShareId": "9d9b2fa0-efbf-490e-a5e3-bac8f7d47354",
                    "Description": "Trip from San Francisco to New York City. Nice trip with two friends. It is a 4 days' trip. We actually had a client meeting, but we also took one to go sightseeings in New York.",
                    "Name": "Trip in US",
                    "Budget": 3000,
                    "StartsAt": "2014-01-01T00:00:00Z",
                    "EndsAt": "2014-01-04T00:00:00Z",
                    "Tags": [
                        "Trip in New York",
                        "business",
                        "sightseeing"
                    ]
                },
                {
                    "TripId": 1003,
                    "ShareId": "f94e9116-8bdd-4dac-ab61-08438d0d9a71",
                    "Description": "Trip from Shanghai to Beijing",
                    "Name": "Trip in Beijing",
                    "Budget": 2000,
                    "StartsAt": "2014-02-01T00:00:00Z",
                    "EndsAt": "2014-02-04T00:00:00Z",
                    "Tags": [
                        "Travel",
                        "Beijing"
                    ]
                },
                {
                    "TripId": 1007,
                    "ShareId": "9ce142c3-5fd6-4a71-848e-5220ebf1e9f3",
                    "Description": "Happy honeymoon trip",
                    "Name": "Honeymoon",
                    "Budget": 2650,
                    "StartsAt": "2014-02-01T00:00:00Z",
                    "EndsAt": "2014-02-04T00:00:00Z",
                    "Tags": [
                        "Travel",
                        "honeymoon"
                    ]
                }
            ]
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400,
            "Friends": [
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
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('scottketchum')/Trips",
            "Trips": [
                {
                    "TripId": 0,
                    "ShareId": "9d9b2fa0-efbf-490e-a5e3-bac8f7d47354",
                    "Description": "Trip from San Francisco to New York City. Nice trip with two friends. It is a 4 days' trip. We actually had a client meeting, but we also took one to go sightseeings in New York.",
                    "Name": "Trip in US",
                    "Budget": 3000,
                    "StartsAt": "2014-01-01T00:00:00Z",
                    "EndsAt": "2014-01-04T00:00:00Z",
                    "Tags": [
                        "Trip in New York",
                        "business",
                        "sightseeing"
                    ]
                },
                {
                    "TripId": 2004,
                    "ShareId": "f94e9116-8bdd-4dac-ab61-08438d0d9a71",
                    "Description": "Trip from Shanghai to Beijing",
                    "Name": "Trip in Beijing",
                    "Budget": 11000,
                    "StartsAt": "2014-02-01T00:00:00Z",
                    "EndsAt": "2014-02-04T00:00:00Z",
                    "Tags": [
                        "Travel",
                        "Beijing"
                    ]
                }
            ]
        },
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
            "Concurrency": 635550870519871400,
            "Friends": [
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
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('scottketchum')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
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
                    "Concurrency": 635550870519871400
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('ronaldmundy')/Trips",
            "Trips": [
                {
                    "TripId": 3009,
                    "ShareId": "dd6a09c0-e59b-4745-8612-f4499b676c47",
                    "Description": "Gradution trip with friends",
                    "Name": "Gradutaion trip",
                    "Budget": 6000,
                    "StartsAt": "2013-05-01T00:00:00Z",
                    "EndsAt": "2013-05-08T00:00:00Z",
                    "Tags": [
                        "Travel"
                    ]
                }
            ]
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
            "Concurrency": 635550870519871400,
            "Friends": [
                {
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
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
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('javieralfred')/Trips",
            "Trips": [
                {
                    "TripId": 4005,
                    "ShareId": "f94e9116-8bdd-4dac-ab61-08438d0d9a71",
                    "Description": "Trip from Shanghai to Beijing",
                    "Name": "Trip in Beijing",
                    "Budget": 800,
                    "StartsAt": "2014-02-01T00:00:00Z",
                    "EndsAt": "2014-02-04T00:00:00Z",
                    "Tags": [
                        "Travel",
                        "Beijing"
                    ]
                }
            ]
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400,
            "Friends": [
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
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('willieashmore')/Trips",
            "Trips": [
                {
                    "TripId": 5007,
                    "ShareId": "5ae142c3-5ad6-4a71-768e-5220ebf1e9f3",
                    "Description": "This is my first business trip",
                    "Name": "Business Trip",
                    "Budget": 3800.5,
                    "StartsAt": "2014-02-01T00:00:00Z",
                    "EndsAt": "2014-02-04T00:00:00Z",
                    "Tags": [
                        "business",
                        "first"
                    ]
                },
                {
                    "TripId": 5008,
                    "ShareId": "9ce32ac3-5fd6-4a72-848e-2250ebf1e9f3",
                    "Description": "The trip is currently in plan.",
                    "Name": "Trip in Europe",
                    "Budget": 2000,
                    "StartsAt": "2014-02-01T00:00:00Z",
                    "EndsAt": "2014-02-04T00:00:00Z",
                    "Tags": [
                        "Travel",
                        "plan"
                    ]
                }
            ]
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
            "Concurrency": 635550870519871400,
            "Friends": [
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
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('willieashmore')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
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
                    "Concurrency": 635550870519871400
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('vincentcalabrese')/Trips",
            "Trips": [
                {
                    "TripId": 7010,
                    "ShareId": "dd6a09c0-e59b-4745-8612-f4499b676c47",
                    "Description": "Gradution trip with friends",
                    "Name": "Gradutaion trip",
                    "Budget": 1000,
                    "StartsAt": "2013-05-01T00:00:00Z",
                    "EndsAt": "2013-05-08T00:00:00Z",
                    "Tags": [
                        "Travel"
                    ]
                }
            ]
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
            "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
            "UserName": "clydeguess",
            "FirstName": "Clyde",
            "LastName": "Guess",
            "Emails": [
                "Clyde@example.com"
            ],
            "AddressInfo": [],
            "Gender": "Male",
            "Concurrency": 635550870519871400,
            "Friends": [
                {
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
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
                    "Concurrency": 635550870519871400
                },
                {
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('ursulabright')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
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
                    "Concurrency": 635550870519871400
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('clydeguess')/Trips",
            "Trips": [
                {
                    "TripId": 8011,
                    "ShareId": "a88f675d-9199-4392-9656-b08e3b46df8a",
                    "Description": "This is a 2 weeks study trip",
                    "Name": "Study trip",
                    "Budget": 1550.3,
                    "StartsAt": "2014-01-01T00:00:00Z",
                    "EndsAt": "2014-01-14T00:00:00Z",
                    "Tags": [
                        "study"
                    ]
                }
            ]
        },
        {
            "@odata.id": "http://services.odata.org/V4/TripPinService/People('keithpinckney')",
            "@odata.etag": "W/\"08D1EE264206F754\"",
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
            "Concurrency": 635550870519871400,
            "Friends": [
                {
                    "@odata.id": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
                    "@odata.etag": "W/\"08D1EE264206F754\"",
                    "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('clydeguess')",
                    "UserName": "clydeguess",
                    "FirstName": "Clyde",
                    "LastName": "Guess",
                    "Emails": [
                        "Clyde@example.com"
                    ],
                    "AddressInfo": [],
                    "Gender": "Male",
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
                }
            ],
            "Trips@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('keithpinckney')/Trips",
            "Trips": []
        }
    ]
}
```

