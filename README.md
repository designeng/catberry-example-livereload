# Catberry Example Project

![Catberry](https://raw.githubusercontent.com/catberry/catberry/master/docs/images/logo.png)

## How to use
This is a simple web-application that works with [GitHub API](http://developer.github.com/)
and demonstrates how to build isomorphic web-application using 
[Catberry Framework](https://github.com/catberry/catberry).

First of all it is needed to install dependencies:

```
npm install
```

Then to start in `debug` mode without script minification and with file watching:

```
npm run debug
```

To start in `release` mode:

```
npm start
```

## Preproduction
Before deploy to production do not forget:

+ to remove `<script>` tag with
```js
document.write('<script src="http://' + (location.host || 'localhost').split(':')[0] +
  ':35729/livereload.js?snipver=1"></' + 'script>')
```
from `catberry_components/document/template.hbs`

+ to remove code
```js
var livereload = require('livereload');
var server = livereload.createServer();
server.watch(__dirname + "/public");
```
from `server.js`.