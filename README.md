# @firanorg/pariatur-officia-placeat <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS WeakSet? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isWeakSet = require('@firanorg/pariatur-officia-placeat');
assert(!isWeakSet(function () {}));
assert(!isWeakSet(null));
assert(!isWeakSet(function* () { yield 42; return Infinity; });
assert(!isWeakSet(Symbol('foo')));
assert(!isWeakSet(1n));
assert(!isWeakSet(Object(1n)));

assert(!isWeakSet(new Set()));
assert(!isWeakSet(new WeakMap()));
assert(!isWeakSet(new Map()));

assert(isWeakSet(new WeakSet()));

class MyWeakSet extends WeakSet {}
assert(isWeakSet(new MyWeakSet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@firanorg/pariatur-officia-placeat
[npm-version-svg]: https://versionbadg.es/inspect-js/@firanorg/pariatur-officia-placeat.svg
[deps-svg]: https://david-dm.org/inspect-js/@firanorg/pariatur-officia-placeat.svg
[deps-url]: https://david-dm.org/inspect-js/@firanorg/pariatur-officia-placeat
[dev-deps-svg]: https://david-dm.org/inspect-js/@firanorg/pariatur-officia-placeat/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@firanorg/pariatur-officia-placeat#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@firanorg/pariatur-officia-placeat.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@firanorg/pariatur-officia-placeat.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@firanorg/pariatur-officia-placeat.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@firanorg/pariatur-officia-placeat
[codecov-image]: https://codecov.io/gh/inspect-js/@firanorg/pariatur-officia-placeat/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@firanorg/pariatur-officia-placeat/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@firanorg/pariatur-officia-placeat
[actions-url]: https://github.com/firanorg/pariatur-officia-placeat/actions
