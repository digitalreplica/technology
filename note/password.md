---
is: "[[note]]"
---
# Notes
- password notes

## Best encryption algorithms
- [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
	- adjustable number of iterations to make cracking more difficult
- [Argon2](https://github.com/p-h-c/phc-winner-argon2) - seems to be an up-and-coming competitor
## Calculating password entropy
A [password entropy calculator](https://www.pleacher.com/mp/mlessons/algebra/entropy.html) equation looks like this:

`E = log2(R^L)`

- E stands for password entropy.
- R stands for possible characters within the password.
- L stands for the number of characters in your password.

Enhance entropy in two steps:
1. **Add more character types.** Include uppercase and lowercase letters, special characters, and numbers.
2. **Increase the length.** Longer passwords have higher scores than shorter versions.

Aim for a score of 60 or higher. But remember: Don't make the password so long and complicated that you'll never remember it.

Sources
- https://www.okta.com/identity-101/password-entropy/
- https://www.omnicalculator.com/math/log-2