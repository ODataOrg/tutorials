**Categories**: C(r)UD

**Description**: To update a resource, send a PATCH request with the properties you wish to modify. You can also use PUT, but the semantics for put require all properties to be either sent on the wire or reverted to their default values. Note: since the People entity set has concurrency enabled, you will need to request the resource and set the If-Match header to the appropriate value to run this request.

**Request**

```js
PATCH http://services.odata.org/V4/TripPinService/People('miathompson')

Accept: application/json
OData-MaxVersion: 4.0
Content-Type: application/json
If-Match: W/"08D1D1EC7DFA1A1B"

{
  "Emails": ["miathompson@contoso.com", "miathompson@example.com"]
}
```

**Response**

```js
204 No Content
```

