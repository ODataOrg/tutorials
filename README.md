# [OData Tutorial Guidelines](http://odataorg.github.io/tutorials/)

##What is this ?

This tutorials covers the scenarios /  features supported by OData V4. The initial version is inspired  by [Basic tutorial](http://www.odata.org/getting-started/basic-tutorial/) and [Understanding OData in 6 steps](http://www.odata.org).

##Why we need this ?

For those who develope OData libraries : This guideline can help you build samples / tutorials / blogs and show users how your product can effectively help them build and consume the RESTful services. 

For those who use OData libraries : you can play with the tools you'd like to choose with this guideline to choose and learn them better.

##How to use this?

 - If you are working on creating your own OData libraries, use these as guidelines to create test cases, samples and blogs. You can link your test cases / sample scenarios / code comments with the .md files directly.
 - If you are using an OData library, with this, you can easily try and tell what futures are supported and what are not (in case the library itself didn't show clearly.)

***Considering that one request per .md file is not easy for users to read thrrough, we use jekyll to generate a [OData Tutorial Guidelines](http://odataorg.github.io/tutorials/) web site from the content in this repository.***

##Structure of this repo

For each OData request, we create one .md file in the [src](https://github.com/ODataOrg/tutorials/tree/master/src) folder in this repository. The .md file is named with the name of the request and hyphen to separate each word, like "read-the-service-root.md" and the name for each .md file will be treated as the identifier of each request in the guideline.

###Template

Below is the Template for the .md file in the pure markdown format. Please do follow this format since we will use this to generate a static site for users to learn these in a better way.

![Template](https://github.com/ODataOrg/tutorials/blob/master/assets/template.png)

You may also refer to a [live example](https://github.com/ODataOrg/tutorials/blob/master/src/read-the-service-root.md).

###Categories
We use the *categories* in the previous template to help generate web site to better render the tutorial guideline. Categories currently supported are:
- Basic Requests
- Filtering Collections
- Other System Query Options
- C(r)UD
- Operations

If you would like to create a new request with a new category, please DO make it stand out in your pull request.

##Contribution
OData always welcome all kinds of contribution. For this tutorial guideline specifically, we try to cover as many secanrios as possible but there are always chances that something missing or not perfect. You can create a pull request with new .md files following the template above or modifying the content of an existing request. 
