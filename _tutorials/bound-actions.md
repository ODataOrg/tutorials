---
name: Bound actions
categories: Operations
---

**Description**: OData support bound custom actions. Actions can have side effects. So the HTTP verb for an OData action can be GET,POST,PUT,DELETE according to the behavior of the action. In the example below, the action implies a POST.

**Request**

```js
POST http://services.odata.org/V4/TripPinService/People('russellwhyte')/Microsoft.OData.SampleService.Models.TripPin.ShareTrip


Accept: application/json
OData-MaxVersion: 4.0
Content-Type: application/json;odata.metadata=minimal

{
"userName": "scottketchum",
"tripId": 0
}
```

**Response**

```js
204 No Content
```

