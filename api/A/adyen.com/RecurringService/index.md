---
slug: "adyen-com-RecurringService"
title: "Adyen Recurring API"
provider: "adyen.com"
description: "The Recurring APIs allow you to manage and remove your tokens or saved\
  \ payment details. Tokens should be created with validation during a payment request.\n\
  \nFor more information, refer to our [Tokenization documentation](https://docs.adyen.com/online-payments/tokenization).\n\
  ## Authentication\nYou need an [API credential](https://docs.adyen.com/development-resources/api-credentials)\
  \ to authenticate to the API.\n\nIf using an API key, add an `X-API-Key` header\
  \ with the API key as the value, for example:\n\n ```\ncurl\n-H \"Content-Type:\
  \ application/json\" \\\n-H \"X-API-Key: YOUR_API_KEY\" \\\n...\n```\n\nAlternatively,\
  \ you can use the username and password to connect to the API using basic authentication,\
  \ for example:\n\n```\ncurl\n-U \"ws@Company.YOUR_COMPANY_ACCOUNT\":\"YOUR_BASIC_AUTHENTICATION_PASSWORD\"\
  \ \\\n-H \"Content-Type: application/json\" \\\n...\n```\n\n## Versioning\nRecurring\
  \ API supports [versioning](https://docs.adyen.com/development-resources/versioning)\
  \ using a version suffix in the endpoint URL. This suffix has the following format:\
  \ \"vXX\", where XX is the version number.\n\nFor example:\n```\nhttps://pal-test.adyen.com/pal/servlet/Recurring/v68/disable\n\
  ```\n\n## Going live\n\nTo authenticate to the live endpoints, you need an [API\
  \ credential](https://docs.adyen.com/development-resources/api-credentials) from\
  \ your live Customer Area.\n\nThe live endpoint URLs contain a prefix which is unique\
  \ to your company account:\n```\n\nhttps://{PREFIX}-pal-live.adyenpayments.com/pal/servlet/Recurring/v68/disable\n\
  ```\n\nGet your `{PREFIX}` from your live Customer Area under **Developers** > **API\
  \ URLs** > **Prefix**."
logo: "adyen.com-RecurringService-logo.svg"
logoMediaType: "image/svg+xml"
tags:
- "payment"
stubs: "adyen.com-RecurringService-stubs.json"
swagger: "adyen.com-RecurringService-swagger.json"
---
