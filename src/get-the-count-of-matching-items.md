---
name: Get the count of matching items
categories: Basic Requests
---

**Description**: If you want to know how many items meet a condition, you can use the $count path segment. Note that the Content-Type header indicates that the content is text/plain. Although it doesn't work with system query options in the reference service, $count can typically be combined with $filter.

**Request**

```
GET http://services.odata.org/V4/TripPinService/People/$count

Accept: */*
OData-MaxVersion: 4.0

```

**Response**

```js
200 OK

20
```