---
is_a: "[[programming language]]"
---
# Notes
Node.js is a server-side focused javascript language

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
	* On mac, can `brew install nvm`. Pay attention to the `~/.zshrc` changes needed.

* Listing installed versions: ```nvm ls```
* Listing all available versions: ```nvm ls-remote```
* Install new version: ```nvm install v12.16.3```
* Use new version: ```nvm use v12.16.3```
* Set default: ```nvm alias default v12.16.3```
* Upgrade npm: `nvm install-latest-npm`

Switching versions: ```nvm use 12.18.3```

## N version manager
N manages multiple version of Node.js
* https://www.npmjs.com/package/n

# Snippets
## Make http request
```
const http = require('http');

let request = http.get('http://{url}/', (res) => { 
	console.log("Inside request");
	console.log(res.statusCode);
	return res;
});
console.log("Outside request");
console.log(process.cwd())
```