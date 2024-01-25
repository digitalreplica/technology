---
is: "[[note]]"
aliases:
  - HSTS
sources:
  - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security
---
# Notes
> The HTTP **`Strict-Transport-Security`** response header (often abbreviated as [HSTS](https://developer.mozilla.org/en-US/docs/Glossary/HSTS)) informs browsers that the site should only be accessed using HTTPS, and that any future attempts to access it using HTTP should automatically be converted to HTTPS.

- no effect for API-type sites, since they're not loaded directly by a browser, rather through a javascript or other client
- 