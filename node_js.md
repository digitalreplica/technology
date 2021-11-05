# Node.js

## Common usages
Initialize app
```
npm init
```

Install dependency
```
npm install <library_name>
```

Install dependency (and save into package.json)
```
npm install --save <library_name>
```

Run simple app
```
node index.js
```

## Mac without sudo
MacOS requires sudo for global installations. This can be avoided.
* [Node and npm without sudo](https://johnpapa.net/node-and-npm-without-sudo/)

# Managing multiple Node versions
## NVM
* https://github.com/nvm-sh/nvm

* Listing installed versions: ```nvm ls```
* Listing all available versions: ```nvm ls-remote```
* Install new version: ```nvm install v12.16.3```
* Use new version: ```nvm use v12.16.3```

Switching versions: ```nvm use 12.18.3```
## N version manager
N manages multiple version of Node.js
* https://www.npmjs.com/package/n
