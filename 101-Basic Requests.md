### 1. Read the service root
All REST APIs should have a single entry point from which a generic hypermedia client can navigate to the resources in the service. In the response we see links to three things: 1. The $metadata document that describes the schema of ther service 2. Links to various collections of objects like People and Airports 3. Links to other top-level items like Me (a singleton) and operations.

```
GET http://services.odata.org/V4/TripPinService/

Accept: application/json
OData-MaxVersion: 4.0
```
