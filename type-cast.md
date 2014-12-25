**Categories**: Filtering collections

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
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('russellwhyte')/Trips(0)/PlanItems/Microsoft.OData.SampleService.Models.TripPin.Flight",
    "value": [
        {
            "PlanItemId": 11,
            "ConfirmationCode": "JH58493",
            "StartsAt": "2014-01-01T06:15:00Z",
            "EndsAt": "2014-01-01T11:35:00Z",
            "Duration": "PT0S",
            "SeatNumber": null,
            "FlightNumber": "AA26"
        },
        {
            "PlanItemId": 13,
            "ConfirmationCode": "JH38143",
            "StartsAt": "2014-01-04T17:55:00Z",
            "EndsAt": "2014-01-04T20:45:00Z",
            "Duration": "PT0S",
            "SeatNumber": null,
            "FlightNumber": "AA4035"
        }
    ]
}
```