---
name: Get a single entity from a collection
categories: Basic Requests
---

**Description**: To get a particular entity from a collection, append a key segment. By default, key segments in OData services are bounded by parens because they may be composite keys, e.g., OrderLine(OrderId=1,LineNumber=1) or alternate keys, e.g., Person(SSN='000-00-0000') and Person(2115) both address the same resource. Some OData services use normal URL segments for key segments, e.g., Orders/1. This is not recommended because of the scenarios mentioned above.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People('russellwhyte')

Accept: application/json
OData-MaxVersion: 4.0

```

**Response**

```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata#People/$entity",
    "@odata.id": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
    "@odata.etag": "W/\"08D1E948E6410AFC\"",
    "@odata.editLink": "http://services.odata.org/V4/TripPinService/People('russellwhyte')",
    "UserName": "russellwhyte",
    "FirstName": "Russell",
    "LastName": "Whyte",
    "Emails": [
        "Russell@example.com",
        "Russell@contoso.com"
    ],
    "AddressInfo": [
        {
            "Address": "187 Suffolk Ln.",
            "City": {
                "CountryRegion": "United States",
                "Name": "Boise",
                "Region": "ID"
            }
        }
    ],
    "Gender": "Male",
    "Concurrency": 635545521745890000
}
```