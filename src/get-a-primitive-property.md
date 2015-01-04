---
name: Get a primitive property
categories: Basic Requests
---

**Description**: Even when fetching a primitive property, an object wrapper is returned rather than returning the raw primitive. This is to protect against a [JSON vulnerability](http://haacked.com/archive/2008/11/20/anatomy-of-a-subtle-json-vulnerability.aspx/).

**Request**

```
GET http://services.odata.org/V4/TripPinService/People('russellwhyte')/FirstName

Accept: application/json
OData-MaxVersion: 4.0

```

**Response**

```js
200 OK

{
"@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('russellwhyte')/FirstName",
"value": "Russell"
}

```