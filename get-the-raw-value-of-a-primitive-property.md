Categories: Basic Requests

If you really want the raw value of a primitive property, you can get it by appending $value to the URL. Note that the Content-Type header indicates that the content is text/plain.

Request

```
GET http://services.odata.org/V4/TripPinService/People('russellwhyte')/FirstName/$value

Accept: */*
OData-MaxVersion: 4.0

```

Response

```js
200 OK

Russell
```