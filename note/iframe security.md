---
is_a: "[[note]]"
topics: "[[security]]"
---
# Notes
- Adding the `sandbox` restricts pretty much all scripts and browser behavior of any kind.
- Can add permissions to set exactly what the iframe is allowed to do

## Most restrictive iframe
```
<iframe sandbox=""></iframe>
```

# References
- https://html.spec.whatwg.org/multipage/iframe-embed-object.html#attr-iframe-sandbox
- https://web.dev/sandboxed-iframes/