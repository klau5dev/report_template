# Google API key with weak restriction is exposed at {{DOMAIN}}

Hi team!

## Summary

I found a Google API key with weak restriction. The key can be used by anyone.

## Steps To Reproduce

1. Find the Google API key

The key can be found at line {{LINE_NUM}} of {{URL}}.
The code is `{{EXPOSED CODE}}`.
And the key is `{{GOOGLE_MAP_API_KEY}}`.

2. Check if the key is alive and can be used by anyone.

- {{GOOGLE_MAP_API_KEY POC LINKS}}

This links confirm that key is alive and can be used by anyone.
I found this key can be used to call {{CALLABLE APIs}} API.

## Impact

If the API keys are not met with the security configurations, below scenarios may be conducted by a malicious user

- A malicious hacker can make financial damage to the company. If the hacker send a lot of Google Map request with this key, the company would consume the company's monthly quota or over-bill. This can be a way of DoS.
- A malicious hacker can use by free or sell the key, but the cost will be paid by the company.

You can check Google Map API price here https://cloud.google.com/maps-platform/pricing/sheet

## How to fix

This article will show you how to keep the Google API key secure. https://cloud.google.com/docs/authentication/api-keys#securing_an_api_key
This restriction should be set, in my opinion. https://cloud.google.com/docs/authentication/api-keys#adding_http_restrictions
