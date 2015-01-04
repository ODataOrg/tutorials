---
name: Navigating the resource graph
categories: Basic Requests
---

**Description**: To navigate the resource graph, keep appending segments representing valid property names as defined in $metadata or in a full metadata response (see query x). In this case we have started from the service root, navigated to the entity set People, navigated to the resource keyed 'russellwhyte', navigated to the Friends property, navigated to the resource keyed 'scottketchum', and finally navigated to the AddressInfo property. Note that the @odata.context URL self-describes the payload.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People('russellwhyte')/Friends('scottketchum')/AddressInfo

Accept: application/json
OData-MaxVersion: 4.0

```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People('russellwhyte')/Friends('scottketchum')/AddressInfo",
    "value": [
        {
            "Address": "2817 Milton Dr.",
            "City": {
                "CountryRegion": "United States",
                "Name": "Albuquerque",
                "Region": "NM"
            }
        }
    ]
}
```