# ActionScript

Jet uses the ActionScript 3 language, fine-tuned.

## Removed features

### Include directive

The `include` directive is not implemented in Jet.

### Default XML namespace

The `default xml namespace =` E4X statement is not implemented in Jet due to WebAssembly limitations.

### Object dynamicness

The `Object` type is not dynamic per se, nor are there dynamic classes. Only the `*` type is dynamic.

- Methods such as `str.match` therefore return an object slightly different than the standard, since `Array` can't be attached properties such as `index`.