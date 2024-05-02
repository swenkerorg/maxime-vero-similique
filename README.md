# @swenkerorg/maxime-vero-similique <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@swenkerorg/maxime-vero-similique');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@swenkerorg/maxime-vero-similique
[npm-version-svg]: https://versionbadg.es/inspect-js/@swenkerorg/maxime-vero-similique.svg
[deps-svg]: https://david-dm.org/inspect-js/@swenkerorg/maxime-vero-similique.svg
[deps-url]: https://david-dm.org/inspect-js/@swenkerorg/maxime-vero-similique
[dev-deps-svg]: https://david-dm.org/inspect-js/@swenkerorg/maxime-vero-similique/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@swenkerorg/maxime-vero-similique#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@swenkerorg/maxime-vero-similique.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@swenkerorg/maxime-vero-similique.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@swenkerorg/maxime-vero-similique.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@swenkerorg/maxime-vero-similique
[codecov-image]: https://codecov.io/gh/inspect-js/@swenkerorg/maxime-vero-similique/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@swenkerorg/maxime-vero-similique/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@swenkerorg/maxime-vero-similique
[actions-url]: https://github.com/inspect-js/@swenkerorg/maxime-vero-similique/actions
