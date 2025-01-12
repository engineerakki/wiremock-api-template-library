---
slug: "climate-com"
title: "Climate FieldView Platform APIs"
provider: "climate.com"
description: "**Last Modified**: Wed Jan  4 12:47:29 UTC 2023\n\n\nAll endpoints are\
  \ only accessible via HTTPS.\n\n* All API endpoints are located at `https://platform.climate.com`\
  \ (e.g.\n`https://platform.climate.com/v4/fields`).\n\n* The authorization token\
  \ endpoint is located at\n`https://api.climate.com/api/oauth/token`.\n\n## Troubleshooting\n\
  \n`X-Http-Request-Id` response header will be returned on every call,\nsuccessful\
  \ or not. If you experience an issue with our api and need\nto contact technical\
  \ support, please supply the value of the `X-Http-Request-Id`\nheader along with\
  \ an approximate time of when the request was made.\n\n## Request Limits\n\nWhen\
  \ you’re onboarded to Climate’s API platform, your `x-api-key` is assigned a custom\
  \ usage plan. Usage plans are unique to each partner and have the following key\
  \ attributes: \n\n1. Throttling information\n    * burstLimit: Maximum rate limit\
  \ over a period ranging from 1 second to a few seconds\n    * rateLimit: A steady-state\
  \ rate limit\n\n2. Quota information\n    * Limit: The maximum number of requests\
  \ that can be made in a given month\n\nWhen the request rate threshold is exceeded,\
  \ a `429` response code is returned. Optionally, the [`Retry-After`](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.37)\
  \ header may be returned: \n\nFollowing are examples of rate limit errors:\n\n1.\
  \ Rate limit exceeded:\n\n<br>HTTP/1.1 429 \n<br>Content-Type: application/json\n\
  <br>Content-Length: 32\n\n   {\"message\":\"Too Many Requests\"}\n\n2. Quota exhausted:\n\
  <br>HTTP/1.1 429 \n<br>Content-Type: application/json\n<br>Content-Length: 29\n\n\
  \    {\"message\":\"Limit Exceeded\"}\n\n## Pagination\n\nPagination is performed\
  \ via headers. Any request which returns a `\"results\"`\narray may be paginated.\
  \ The following figure shows how query results are laid out with\nX-Limit=4 and\
  \ no filter applied.\n\n<img style=\"width:70%;height:auto;\" src=\"https://s3-us-west-2.amazonaws.com/climate-com/images/svg_upload_tests/paging.png\"\
  >\n\n* If there are no results, a response code of `304` will be returned.\n\n*\
  \ If the response is the last set of results, a response code of `200` or\n`206`\
  \ will be returned.\n\n* If there are more results, a response code of `206` will\
  \ be returned.\n\n* If `X-Next-Token` is provided in the request headers but the\
  \ token has\nexpired, a response code of `409` will be returned. This is only applicable\n\
  for some endpoints; see specific endpoint documentation below.\n\n#### X-Limit\n\
  \nThe page size can be controlled with the `X-Limit` header. Valid values are\n\
  `1-100` and defaults to `100`.\n\n#### X-Next-Token\n\nIf the results are paginated,\
  \ a response header of `X-Next-Token` will be\nreturned. Use the associated value\
  \ in the subsequent request (via the `X-Next-Token`\nrequest header) to retrieve\
  \ the next page. The following sequence diagram shows how to\nuse `X-Next-Token`\
  \ to fetch all the records.\n\n<img src=\"https://s3-us-west-2.amazonaws.com/climate-com/images/svg_upload_tests/x-next-token.svg\"\
  >\n\n\n## Chunked Uploads\n\nUploads larger than `5MiB` (`5242880 bytes`) must be\
  \ done in `5MiB` chunks\n(with the exception of the final chunk). Each chunk request\
  \ MUST contain a\n`Content-Range` header specifying the portion of the upload, and\
  \ a `Content-Type`\nheader specifying binary content type (`application/octet-stream`).\
  \ Range\nuploads must be contiguous. The maximum upload size is capped at `500MiB`\
  \ (`524288000 bytes`).\n\n## Chunked Downloads\n\nDownloads larger than `5MiB` (`5242880\
  \ bytes`) must be done in `1-5MiB`\nchunks (with the exception of the final chunk,\
  \ which may be less than `1MiB`).\nEach chunk request MUST contain a `Range` header\
  \ specifying the requested portion of the download,\nand an `Accept` header specifying\
  \ binary and json content types  (`application/octet-stream,application/json`)\n\
  or all content types (`*/*`).\n\n## Drivers\n\nIf you need drivers to process agronomic\
  \ data, download the ADAPT plugin below. We only support the plugin in the Windows\
  \ environment, minimum is Windows 7 SP1.\n\nFor asPlanted, asHarvested and asApplied\
  \ data:\n* [ADAPT Plugin](https://dev.fieldview.com/drivers/ClimateADAPTPlugin_latest.exe)\n\
  <br>Release notes can be found [here](https://dev.fieldview.com/drivers/adapt-release-notes.txt).\n\
  <br>Download and use of the ADAPT plugin means that you agree to the EULA for use\
  \ of the ADAPT plugin. \n<br>Please review the [EULA](https://dev.fieldview.com/EULA/ADAPT%20Plugin%20EULA-06-19.pdf)\
  \ (last updated on June 6th, 2019) before download and use of the ADAPT plugin.\n\
  <br>For more information, please refer to:\n  * [ADAPT Resources](https://adaptframework.org/)\n\
  \  * [ADAPT Overview](https://aggateway.atlassian.net/wiki/spaces/ADM/overview)\n\
  \  * [ADAPT FAQ](https://aggateway.atlassian.net/wiki/spaces/ADM/pages/165942474/ADAPT+Frequently-Asked+Questions+FAQ)\n\
  \  * [ADAPT Videos](https://adaptframework.org/adapt-videos/)\n\n## Sample Test\
  \ Data\n\nSample agronomic data:\n* [asPlanted and asHarvested data](https://dev.fieldview.com/sample-agronomic-data/Planting_Harvesting_data_04_18_2018_21_46_18.zip)\n\
  * [asApplied data set 1](https://dev.fieldview.com/sample-agronomic-data/as-applied-data1.zip)\n\
  * [asApplied data set 2](https://dev.fieldview.com/sample-agronomic-data/as-applied-data2.zip)\n\
  <br>To upload the sample data to your account, please follow the instructions in\
  \ this [link](https://support.climate.com/kt#/kA02A000000AaxzSAC/en_US).\n\nSample\
  \ soil data:\n* [Sample soil data](https://dev.fieldview.com/sample-soil-data/soil-sample.xml)\n\
  ---\n"
logo: "climate.com-logo.svg"
logoMediaType: "image/svg+xml"
tags:
- "open_data"
stubs: "climate.com-stubs.json"
swagger: "climate.com-swagger.json"
---
