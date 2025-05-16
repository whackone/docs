# ActionScript

Jet uses the ActionScript 3 language, fine-tuned.

## Changed/removed features

### Include directive

The `include` directive is not implemented in Jet.

### Default XML namespace

The `default xml namespace =` E4X statement is not implemented in Jet due to WebAssembly limitations.

### Object dynamicness

The `Object` type is not dynamic per se, nor are there dynamic classes. Only the `*` type is dynamic.

- Methods such as `str.match` therefore return an object slightly different than the standard, since `Array` can't be attached properties such as `index`.

### “in” operator behavior

The `in` operator behaves differently. It triggers `jet_proxy::has()` which is in general used for determining whether a collection contains a specific value; for `Map`s it determines whether a pair key exists; for `XML` and `XMLList` objects it performs the same E4X behavior.