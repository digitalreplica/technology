---
is_a: "[[note]]"
---
# Notes
- config file in `~/.ssh/config`

Using a standalone private key
```
ssh -i id_rsa user@ip
```

ssh through jumpbox
```
ssh -J myuser@jumpbox myuser@securebox
```

Config file - which key file to use for host
```
Host myserver.com
  IdentityFile ~/.ssh/id_dsa
  User ubuntu
```

Config file - proxy host
```
Host host2
  ProxyJump host1
```