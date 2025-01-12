---
slug: "pendo-io"
title: "Pendo Feedback API"
provider: "pendo.io"
description: "## Who is this for?\n\nThis documentation is for developers creating\
  \ their own integration with [Feedback's](https://www.pendo.io/product/feedback/)\
  \ API. If you are doing a standard integration, there's a really easy [Javascript\
  \ integration](https://help.receptive.io/hc/en-us/articles/209221969-How-to-integrate-Receptive-with-your-app)\
  \ that you should know about before you go to the effort of building your own integration.\n\
  \n## Authentication\n\nAPI calls generally need to be authenticated. Generate an\
  \ API Key at https://feedback.pendo.io/app/#/vendor/settings?section=integrate.\
  \ This key should then be added to every request as a request header named 'auth-token'\
  \ (preferred), or as a query parameter named 'auth-token'.\n\n## Endpoint\n\nAPI\
  \ endpoint is https://api.feedback.eu.pendo.io / https://api.feedback.us.pendo.io\
  \ depending where your datacenter is located.\n\n## Notes\n\nAPI endpoints are being\
  \ added to this documentation as needed by customers. If you don't see an endpoint\
  \ you need please contact support and if it exists we'll publish the docs here.\
  \ The 'try it out' feature on this documentation page will probably be blocked by\
  \ your browser because the Access-Control-Allow-Origin header has its value set\
  \ by the Feedback server depending on your hostname.\n\n## Generating client code\n\
  \nThis documentation is automatically generated from an OpenAPI spec available [here](http://apidoc.receptive.io/receptive.swagger.json).\
  \ You can use Swagger to auto-generate API client code in many languages using the\
  \ [Swagger Editor](http://editor.swagger.io/#/)"
logo: "pendo.io-logo.jpeg"
logoMediaType: "image/jpeg"
tags:
- "ecommerce"
stubs: "pendo.io-stubs.json"
swagger: "pendo.io-swagger.json"
---
