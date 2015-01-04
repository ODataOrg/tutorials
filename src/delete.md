---
name: Delete
categories: C(r)UD
---

**Description**: To remove a resource, send an HTTP DELETE to the resource URL. Note: since the People entity set has concurrency enabled, you will need to request the resource and set the If-Match header to the appropriate value to run this request.

**Request**

```js
DETELE http://services.odata.org/V4/TripPinService/People('miathompson')

Accept: application/json
OData-MaxVersion: 4.0
If-Match: W/"08D1EE2853C601AC"
```

**Response**

```js
204 No Content
```

