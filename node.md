#Node.js Cheatsheet


###Detecting Memory Leaks in Node

- [How To Self Detect A Memory Leak in Node](http://www.nearform.com/nodecrunch/self-detect-memory-leak-node/)

###Managing Dependency Collisions

- [Managing Node.js Dependencies with Shrinkwrap](http://blog.nodejs.org/2012/02/27/managing-node-js-dependencies-with-shrinkwrap/)

###Learning node.js

- [NodeSchool](http://nodeschool.io/)

###Debugging node

- [TEN TIPS FOR CODING WITH NODE.JS #1: DEVELOP DEBUGGING TECHNIQUES](http://www.nearform.com/nodecrunch/node-js-develop-debugging-techniques/)

###Testing Node

- [Node.js Testing Strategies](http://www.pluralsight.com/courses/nodejs-testing-strategies)

###Shell scripts in Node

- [Write your shell scripts in JavaScript, via Node.js](http://www.2ality.com/2011/12/nodejs-shell-scripting.html)

To make a javascript file executable, run this command to change its permissions:
```
$ chmod u+x myscript.js
```
And make sure you have the proper shebang in your javascript file (myscript.js):

```js
#!/usr/bin/env node
```

###Node CLI

- [minimist](https://github.com/substack/minimist)

###Node Security

- [Secure Node Apps Against OWASP Top 10](http://scottksmith.com/blog/2015/06/08/secure-node-apps-against-owasp-top-10-injection/)
- [Top Overlooked Security threats to Node.js Web Applications](https://speakerdeck.com/player/c5d895008c77013162b85e7a2e8ee0d7)

###Run ES6 in node

To run ES6 code in Node.js:

1. Make sure babel is installed
`$ npm install -g babel`

2. Now you can run "babel-node" instead of "node"
`$ babel-node file-with-es6-js.js`

###Design Patterns

- [Fundamental Node.js Design Patterns](https://blog.risingstack.com/fundamental-node-js-design-patterns/)

###OpenGraph

- [Get Open Graph Data with Node.js](http://davidwalsh.name/open-graph-data-nodejs)