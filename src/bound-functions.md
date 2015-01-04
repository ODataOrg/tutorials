---
name: Bound functions
categories: Operations
---

**Description**: OData support bound custom functions. The bound functions are bounded to a resource. Note: OData functions CANNOT have side effect, so only GET verb is allowed.

**Request**

```js
GET http://services.odata.org/V4/TripPinService/People('russellwhyte')/Microsoft.OData.SampleService.Models.TripPin.GetFavoriteAirline()

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
	"@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#Airlines/$entity",
	"@odata.id": "http://services.odata.org/V4/TripPinService/Airlines('AA')",
	"@odata.editLink": "http://services.odata.org/V4/TripPinService/Airlines('AA')",
	"AirlineCode": "AA",
	"Name": "American Airlines"
}
```

