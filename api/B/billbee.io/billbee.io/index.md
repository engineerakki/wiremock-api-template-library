---
slug: "billbee-io"
title: "Billbee API"
provider: "billbee.io"
description: "Documentation of the Billbee REST API to connect a Billbee account to\
  \ external aplications.\n\n## Endpoint\n\nThe Billbee API endpoint base url is https://api.billbee.io/api/v1\
  \ \n\n## Activation\n\nYou have to enable the API in the settings of your Billbee\
  \ account. In addition you need a Billbee API Key identifying the application you\
  \ develop. To get an API key, send a mail to support@billbee.io and send us a short\
  \ note about what you are building.\n\n## Authorization & security\n\nBecause you\
  \ can access private data with the Billbee API, every request has to be sent over\
  \ https and must\n\n* Contain a valid API Key identifying the application/developer.\
  \ It has to be sent as the HTTP header X-Billbee-Api-Key\n* Contain a valid user\
  \ login with billbee username and api password in form of a basic auth HTTP header\n\
  \n## Throttling\n\nEach endpoint has a throttle of max 2 requests per second per\
  \ combination of API Key and Billbee user.\n\nWhen you exceed these 2 calls, the\
  \ API will return a HTTP 429 status code\n\n"
logo: "billbee.io-logo.png"
logoMediaType: "image/png"
tags:
- "ecommerce"
stubs: "billbee.io-stubs.json"
swagger: "billbee.io-swagger.json"
---
