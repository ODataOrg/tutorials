# OData Tutorial Guidelines

**What is this ?**

This tutorials covers the scenarios /  features supported by OData V4. The initial version is inspired  by [Basic tutorial](http://www.odata.org/getting-started/basic-tutorial/) and [Understanding OData in 6 steps](http://www.odata.org).

**Why we need this ?**

For those who develope OData libraries : This guideline can help you build samples / tutorials / blogs and show users how your product can effectively help them build and consume the RESTful services. 

For those who use OData libraries : you can play with the tools you'd like to choose with this guideline to choose and learn them better.

**How to use this?**

 - If you are working on creating your own OData libraries, use these as guidelines to create test cases, samples and blogs. You can link your test cases / sample scenarios / code comments with the .md files directly.
 - If you are using an OData library, with this, you can easily try and tell what futures are supported and what are not (in case the library itself didn't show clearly.)

**Structure of this repo**

For each OData request, we create one .md file in the repo. The .md file is named with the name of the request and hyphen to separate each word, like "read-the-service-root.md" and the name for each .md file will be treated as the identifier of each request in the guideline.

*Template for the .md file*
Categories: category name
Description 
Request 
```
HTTP verb, request URL
HTTP headers 
Request body
```
Response 
```
HTTP response code
HTTP response body
```

*Example :  read-the-service-root.md*
Category: basic requests
Request
```js
GET http://services.odata.org/V4/TripPinService/

Accept: application/json
OData-MaxVersion: 4.0

```
Response
```js
200 OK

{
    "@odata.context": "http://services.odata.org/V4/TripPinService/$metadata",
    "value": [
        {
            "name": "Photos",
            "kind": "EntitySet",
            "url": "Photos"
        },
        {
            "name": "People",
            "kind": "EntitySet",
            "url": "People"
        },
        {
            "name": "Airlines",
            "kind": "EntitySet",
            "url": "Airlines"
        },
        {
            "name": "Airports",
            "kind": "EntitySet",
            "url": "Airports"
        },
        {
            "name": "Me",
            "kind": "Singleton",
            "url": "Me"
        },
        {
            "name": "GetNearestAirport",
            "kind": "FunctionImport",
            "url": "GetNearestAirport"
        }
    ]
}
```

**Contribution**
OData always welcome all kinds of contribution. For this tutorial guideline specifically, we try to cover as many secanrios as possible but there are always chances that something missing or not perfect. You can create a pull request with new .md files following the template above or modifying the content of an existing request. 
