---
is: "[[note]]"
aliases:
  - CSP header
  - Content-Security-Policy
of:
  - "[[http]]"
  - "[[security]]"
urls: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy
---
# Notes
- The more modern http header to control many browser security settings for given website or domain
- The two most important directives are the `frame-ancestors` and 

## Frame Ancestors
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors
- Controls which sites are allowed to iframe the content of a given site

## script-src
- The `script-src` directive controls which javascript resources should be loaded and executed. When set, javascript from non-allowed sites will not be loaded or executed.