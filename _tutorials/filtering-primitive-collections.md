---
name: Filtering primitive collections
categories: Filtering Collections
---

**Description**: You can filter any type of collection in OData services. When referring to a member of the collection, you can use $it as reference to the member itself.

**Request**

```
GET 

Accept: application/json
OData-MaxVersion: 4.0
```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('ronaldmundy')/Emails",
    "value": [
        "Ronald@example.com"
    ]
}
```