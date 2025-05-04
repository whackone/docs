# Types

## void

```
void // undefined
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

The `Array` type is optimized for when `T` is a number.

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

## Object

```
{
    /** x */
    x:Number,

    /** y */
    y?:Boolean,
}
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