# @diotoborg/et-voluptatum-mollitia <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Set? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isSet = require('@diotoborg/et-voluptatum-mollitia');
assert(!isSet(function () {}));
assert(!isSet(null));
assert(!isSet(function* () { yield 42; return Infinity; });
assert(!isSet(Symbol('foo')));
assert(!isSet(1n));
assert(!isSet(Object(1n)));

assert(!isSet(new Map()));
assert(!isSet(new WeakSet()));
assert(!isSet(new WeakMap()));

assert(isSet(new Set()));

class MySet extends Set {}
assert(isSet(new MySet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@diotoborg/et-voluptatum-mollitia
[npm-version-svg]: https://versionbadg.es/inspect-js/@diotoborg/et-voluptatum-mollitia.svg
[deps-svg]: https://david-dm.org/inspect-js/@diotoborg/et-voluptatum-mollitia.svg
[deps-url]: https://david-dm.org/inspect-js/@diotoborg/et-voluptatum-mollitia
[dev-deps-svg]: https://david-dm.org/inspect-js/@diotoborg/et-voluptatum-mollitia/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@diotoborg/et-voluptatum-mollitia#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@diotoborg/et-voluptatum-mollitia.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@diotoborg/et-voluptatum-mollitia.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@diotoborg/et-voluptatum-mollitia.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@diotoborg/et-voluptatum-mollitia
[codecov-image]: https://codecov.io/gh/inspect-js/@diotoborg/et-voluptatum-mollitia/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@diotoborg/et-voluptatum-mollitia/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@diotoborg/et-voluptatum-mollitia
[actions-url]: https://github.com/diotoborg/et-voluptatum-mollitia/actions
