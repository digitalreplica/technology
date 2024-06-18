---
is_a: "[[note]]"
topics: 
in: 
---
# Notes
- https://oauth.net/2/
- Open authentication mechanism
- Terms
	- client: application
	- resource owner: user
- Confidential clients can keep a secret. Usually server-side
- Public clients cant. Like public web apps, browser downloads entire app, so attackers can look for secrets

Oauth v2 changing implicit flow
- never really secure
- to do it properly requires a cross-domain POST blocked by browser security settings
- now better mechanisms to do that securely
- challenge is places where redirect URL can be intercepted: proxies, captive portals, browser extensions
- Guidance from Oauth working group is keep existing apps using implicit flow, build new apps with [[PKCE]] and code authorization flow.