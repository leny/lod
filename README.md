# lòd

> Change the order of an array

* * *

## Getting Started

### From **browsers** and **node**.

Install the module with: `npm install lod`.

> **NOTE:** lòd use the ES6 module definition. For now, it uses Babel to transpile to ES5.  
> So, if you use ES5, you should require lòd with `var lod = require( "lod" ).default;`, and, if you use ES6, you should import lòd with `import lod from "lod";`.

## Documentation

**lòd** returns a new, reordered version of an array, using another array of ordered indexes.

### Signature

`reordered_array = lod( source_array, order_array );`

#### Example

```javascript
var lod = require( "lod" ).default;

var source_array = [ "one", "two", "three", "four" ];

var reordered_array = lod( source_array, [ 2, 3, 0, 1 ] ); // [ "three", "four", "one", "two" ]
```

See [tests](./test/lod_test.js) for other examples.

### Restrictions & errors

* **lòd** will throw a `Error( "INVALID_ORDER_CONTENT" )` if the `order_array` contains elements that are not **Number**.

* **lòd** will throw a `Error( "OUT_OF_BOUNDS_ORDER_INDEX" )` if the `order_array` contains numbers that are not inside the `source_array` range.

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## License
(Un)licensed under the UNLICENSE
