# String.prototype.trimStart <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES2019-spec-compliant `String.prototype.trimStart` shim. Invoke its "shim" method to shim `String.prototype.trimStart` if it is unavailable.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the [spec](https://www.ecma-international.org/ecma-262/6.0/#sec-object.assign). In an ES6 environment, it will also work properly with `Symbol`s.

Most common usage:
```js
var trimStart = require('@hishprorg/aliquid-ad-vero');

assert(trimStart(' \t\na \t\n') === 'a \t\n');

if (!String.prototype.trimStart) {
	trimStart.shim();
}

assert(trimStart(' \t\na \t\n') === ' \t\na \t\n'.trimStart());
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@hishprorg/aliquid-ad-vero
[npm-version-svg]: https://vb.teelaun.ch/hishprorg/aliquid-ad-vero.svg
[deps-svg]: https://david-dm.org/hishprorg/aliquid-ad-vero.svg
[deps-url]: https://david-dm.org/hishprorg/aliquid-ad-vero
[dev-deps-svg]: https://david-dm.org/hishprorg/aliquid-ad-vero/dev-status.svg
[dev-deps-url]: https://david-dm.org/hishprorg/aliquid-ad-vero#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@hishprorg/aliquid-ad-vero.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@hishprorg/aliquid-ad-vero.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@hishprorg/aliquid-ad-vero.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@hishprorg/aliquid-ad-vero
[codecov-image]: https://codecov.io/gh/hishprorg/aliquid-ad-vero/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/hishprorg/aliquid-ad-vero/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/hishprorg/aliquid-ad-vero
[actions-url]: https://github.com/hishprorg/aliquid-ad-vero/actions
