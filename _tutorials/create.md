---
name: Create
categories: C(r)UD
---

**Description**: To create a resource, send a POST to a collection.

**Request**

```js
POST http://services.odata.org/V4/TripPinService/People

Accept: application/json
OData-MaxVersion: 4.0
Content-Type: application/json

{
  "UserName": "miathompson",
  "FirstName": "Mia",
  "LastName": "Thompson",
  "Gender": "Female"
}
```

**Response**

```js
201 Created

{
	"@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People/$entity",
	"@odata.id": "http://services.odata.org/V4/TripPinService/People('miathompson')",
	"@odata.etag": "W/\"08D1EE27D0A34606\"",
	"@odata.editLink": "http://services.odata.org/V4/TripPinService/People('miathompson')",
	"UserName": "miathompson",
	"FirstName": "Mia",
	"LastName": "Thompson",
	"Emails": [ ],
	"AddressInfo": [ ],
	"Gender": "Female",
	"Concurrency": 635550877207447046
}
```

