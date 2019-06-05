# merge-descriptors

[![NPM Version][npm-image]][npm-url]
[![NPM Downloads][downloads-image]][downloads-url]
[![Build Status][travis-image]][travis-url]
[![Test Coverage][coveralls-image]][coveralls-url]

Merge source object properties onto a destination object, and preserve 
descriptors. Descriptors are configuration data associated to each property 
such as whether the property is `writable`, `enumerable`, and/or `configurable`.
This data will be preserved in the destination object.

```js
var thing = {
  get name() {
    return 'jon'
  }
}

var animal = {

}

merge(animal, thing)

animal.name === 'jon'
```

## API

### merge(destination, source, overwrite)

Merge properties from `source` object onto `destination` object, preserving 
each property's descriptors. The `overwrite` argument is optional and has 
default value `true`. If `overwrite == true` then existing properties on 
`destination` will be overwritten. If `overwrite == false`, existing properties 
on `destination` will not be overwritten. Returns the destination object.

## License

[MIT](LICENSE)

[npm-image]: https://img.shields.io/npm/v/merge-descriptors.svg
[npm-url]: https://npmjs.org/package/merge-descriptors
[travis-image]: https://img.shields.io/travis/component/merge-descriptors/master.svg
[travis-url]: https://travis-ci.org/component/merge-descriptors
[coveralls-image]: https://img.shields.io/coveralls/component/merge-descriptors/master.svg
[coveralls-url]: https://coveralls.io/r/component/merge-descriptors?branch=master
[downloads-image]: https://img.shields.io/npm/dm/merge-descriptors.svg
[downloads-url]: https://npmjs.org/package/merge-descriptors
