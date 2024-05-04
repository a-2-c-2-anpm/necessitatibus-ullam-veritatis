# @a-2-c-2-anpm/necessitatibus-ullam-veritatis <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Proposal spec-compliant shim for Set.prototype.isSubsetOf. Invoke its "shim" method to shim `Set.prototype.isSubsetOf` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment, and complies with the [proposed spec](https://github.com/tc39/proposal-set-methods). When shimmed, it uses [`es-set`](https://npmjs.com/es-set) to shim the `Set` implementation itself if needed.

Most common usage:
```js
var assert = require('assert');
var isSubsetOf = require('@a-2-c-2-anpm/necessitatibus-ullam-veritatis');

var set1 = new Set([1, 2]);
var set2 = new Set([2, 3]);
var set3 = new Set([1]);

assert.equal(isSubsetOf(set1, set2), false);
assert.equal(isSubsetOf(set2, set1), false);
assert.equal(isSubsetOf(set3, set1), true);

isSubsetOf.shim();

assert.equal(set1.isSubsetOf(set2), false);
assert.equal(set2.isSubsetOf(set1), false);
assert.equal(set3.isSubsetOf(set1), true);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Set Method Packages
 - [union](https://npmjs.com/set.prototype.union)
 - [intersection](https://npmjs.com/set.prototype.intersection)
 - [difference](https://npmjs.com/set.prototype.difference)
 - [symmetricDifference](https://npmjs.com/set.prototype.symmetricdifference)
 - [isSubsetOf](https://npmjs.com/@a-2-c-2-anpm/necessitatibus-ullam-veritatis)
 - [isSupersetOf](https://npmjs.com/set.prototype.issupersetof)
 - [isDisjointFrom](https://npmjs.com/set.prototype.isdisjointfrom)

[package-url]: https://npmjs.com/package/@a-2-c-2-anpm/necessitatibus-ullam-veritatis
[npm-version-svg]: http://versionbadg.es/a-2-c-2-anpm/necessitatibus-ullam-veritatis.svg
[deps-svg]: https://david-dm.org/a-2-c-2-anpm/necessitatibus-ullam-veritatis.svg
[deps-url]: https://david-dm.org/a-2-c-2-anpm/necessitatibus-ullam-veritatis
[dev-deps-svg]: https://david-dm.org/a-2-c-2-anpm/necessitatibus-ullam-veritatis/dev-status.svg
[dev-deps-url]: https://david-dm.org/a-2-c-2-anpm/necessitatibus-ullam-veritatis#info=devDependencies
[testling-svg]: https://ci.testling.com/a-2-c-2-anpm/necessitatibus-ullam-veritatis.png
[testling-url]: https://ci.testling.com/a-2-c-2-anpm/necessitatibus-ullam-veritatis
[npm-badge-png]: https://nodei.co/npm/@a-2-c-2-anpm/necessitatibus-ullam-veritatis.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@a-2-c-2-anpm/necessitatibus-ullam-veritatis.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@a-2-c-2-anpm/necessitatibus-ullam-veritatis.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@a-2-c-2-anpm/necessitatibus-ullam-veritatis
[codecov-image]: https://codecov.io/gh/a-2-c-2-anpm/necessitatibus-ullam-veritatis/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/a-2-c-2-anpm/necessitatibus-ullam-veritatis/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/a-2-c-2-anpm/necessitatibus-ullam-veritatis
[actions-url]: https://github.com/a-2-c-2-anpm/necessitatibus-ullam-veritatis/actions
