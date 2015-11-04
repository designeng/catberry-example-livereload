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
Before deploy to production do not forget to remove `<script>` tag with
```js
document.write('<script src="http://' + (location.host || 'localhost').split(':')[0] +
  ':35729/livereload.js?snipver=1"></' + 'script>')
```
from `catberry_components/document/template.hbs`.

## Contribution
If you have found a bug, please create pull request with [mocha](https://www.npmjs.org/package/mocha) 
unit-test which reproduces it or describe all details in an issue if you can not
implement test. If you want to propose some improvements just create an issue or
a pull request but please do not forget to use `npm test` to be sure that your
code is awesome.

All changes should satisfy this [Code Style Guide](https://github.com/catberry/catberry/blob/4.0.0/docs/code-style-guide.md).

Also your changes should be covered by unit tests using [mocha](https://www.npmjs.org/package/mocha).

Denis Rechkunov <denis.rechkunov@gmail.com>
