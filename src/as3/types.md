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

String is a UTF-16 encoded sequence of characters.

```
String
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

Tuples, when untyped, have the `length` property available.

```
[T1, T2]
```

## Array

The `Array` type represents a dynamic list of elements, optimized for when `T` is a number; for instance, `[uint]` will use a growable buffer optimized specifically for 32-bit unsigned integers.

```
[T]
```

## Structural function

Structural function types inherit from `Function`.

```
function(T1, T2=, ...[T3]):E
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

> **Note:** Property access on a `Map` equals data access. Method call on a `Map` equals `Map` method use.

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

`...rest` components may appear, where `rest` must be another structural object type; the resulting type may be a subtype of `rest` depending on whether properties do not collide.

```
type A = { x:Number };
type B = { y:Number, ...A };
type U = { ...W, ...B };
type W = { z:Number };
```

## Objects

All types except `void`, `null`, `uint`, `int`, `float`, `Number` and `Boolean` represent referenceable objects that may be `null`. The `Object` class is inherited by all types, except `*`, `void`, `null` and unions.

The `Object` class, unlike in standard ActionScript, is not untyped and there is no support for `dynamic` classes; therefore, it is preferable to use the `*` type when it is necessary to access prototype properties such as `constructor` and `toString()`.