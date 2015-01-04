---
name: Built-in functions
categories: Filtering Collections
---

**Description**: Another way of filtering items is to use a type cast segment. In this case we are looking for all of the flights that are part of Russell's trip. A type cast also allows us to append additional path segments that are properties of the subtype.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People('russellwhyte')/Trips(0)/PlanItems/Microsoft.OData.SampleService.Models.TripPin.Flight

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('russellwhyte')/Trips",
    "value": [
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
}
```