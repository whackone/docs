# Types

## Wildcard

The `*` type means untyped, and accepts all possible values in the language.

```
*
```

## void

```
void // undefined
```

## null

```
null // null
```

## String

String is a UTF-8 encoded sequence of characters.

> **Note**: This data type differs from the standard ActionScript 3 string data type in the encoding.

```
String // UTF-8 encoded string
```

## Boolean

```
Boolean // false or true
```

## Number

```
Number // double-precision floating point
```

## float

```
float // single-precision floating point
```

## int

```
int // signed 32-bit integer
```

## uint

```
uint // unsigned 32-bit integer
```

## Tuple

```
[T1, T2]
```

## Array

The `Array` type represents a dynamic list of elements, optimized for when `T` is a number; for instance, `[uint]` will use a growable buffer optimized specifically for 32-bit unsigned integers.

```
[T]
```

## Function

```
function(T1, T2=, ...T3):E
```

## Union

```
(Ta, Tb)
```

## Map

```
Map.<K, V>
```

Usage instance:

```
const map = new Map.<String, Number>();
map.x = 10;

const fns = new Map.<String, Function>();
fns.m = function() { return 10 };
trace(fns.call("m"));
```

## Structural object

Structural object types are compiled into efficient structures.

```
{
    /** x */
    x:Number,

    /** y */
    y?:Boolean,
}
```

A single `...rest` component may appear as the last item, where `rest` must be another structural object type; the resulting type is a subtype of `rest`, and properties are not allowed to collide.

```
{
    y:Number,
    ...A
}
```

## Objects

All types except `void`, `null`, `uint`, `int`, `float`, `Number` and `Boolean` represent referenceable objects. The `Object` class is inherited from all types, except `*`, `void` and `null`, which are not classes.