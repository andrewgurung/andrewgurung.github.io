---
layout: post
title: Getting Started with Node.js
comments: true
---

### Getting Node.js
There are different ways of getting Node.js:
1. Downloading installers or binaries
  - https://nodejs.org/en/download/
2. Build from source code
3. For OSX and Linux environment, manage multiple version using `nvm` tool
  - We will be installing Node.js using the `nvm` tool for OSX

### Installing Node Version Manager `nvm` tool
- Manual install of nvm:
```shell
$ git clone https://github.com/creationix/nvm.git ~/nvm
```

- Use `source` command load function file(nvm.sh) into the command prompt:
```shell
$ . ~/nvm/nvm.sh
```

- Test nvm:
```shell
$ nvm
```

### Installing Node.js using `nvm` tool
- Install multiple versions of node:
```shell
$ nvm install v4.4.2
$ nvm install v5.10.1
```

- List installed node versions:
```shell
$ nvm ls
```

- Display current version:
```shell
$ node -v
```

- Switch node version:
```shell
$ nvm use v4.2.2
```

- Set Alias default:
```shell
$ nvm alias default v5.10.1
```

- Run node (Enters REPL[Read Eval Print Loop] Terminal):
```shell
$ node
> console.log("Node Intro");
Hello World
undefined
>
(^C again to quit)
>
##
```

### Running a simple web server
- Create a `server.js` file
  ```js
  const http = require('http');

  const hostname = '127.0.0.1';
  const port = 1337;

  http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Node Intro\n');
  }).listen(port, hostname, () => {
    console.log(`Server running at http://${hostname}:${port}/`);
  });
  ```
- Then run `$ node server.js`
- Open `http://127.0.0.1:1337` in browser to test your simple web server
