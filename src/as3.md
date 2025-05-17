# ActionScript

Jet uses the ActionScript 3 language, fine-tuned.

## Changed features

### String type

The `String` type stores Unicode Code Points (UTF-32), not UTF-16 code units.

```
const s = "\u{10000}a";
assert( s.charCodeAt(1) == "a".charCodeAt(0) );
```

### Include directive

The `include` directive is not implemented in Jet.

### Default XML namespace

The `default xml namespace =` E4X statement is not implemented in Jet due to WebAssembly limitations.

### Object dynamicness

The `Object` type is not dynamic per se, nor are there dynamic classes. Only the `*` type is dynamic.

- Methods such as `str.match` therefore return an object slightly different than the standard, since `Array` can't be attached properties such as `index`.

### “in” operator

The `in` operator behaves differently. It triggers `jet_proxy::has()` which is in general used for determining whether a collection contains a specific value; for `Map`s it determines whether a pair key exists; for `XML` and `XMLList` objects it performs the same E4X behavior.

### Filter operator

The filter operator has been modified to take a local (`.(pattern_name, test)`) rather than cluttering the lexical scope.

```
xnode.(o, o.@x.startsWith("abc"))
```

### With statement

The with statement is not implemented since using it with dynamic types such as `XML` clutters the lexical scope.

### “this” capture

The `this` object is always captured from the parent activation in nested activations; there is no way to override the `this` object with another value.

### Available packages

Available packages depend on the dependencies table of the Jet manifest. Jet will not make undepended package definitions part of the program; `as3.lang` and `jet.base` are always part of the program.