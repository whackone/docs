# Classes

## Inheritance

By default a class extends `Object`. Use the `extends` clause for extending a specific class:

```
class B extends A {}
```

## Constructor

By default the constructor is based in the base class's constructor and will initialize the instance with default property values.

Define a constructor for a class using its name in a function definition:

```
class A {
    public function A() {}
}
```

## Abstract classes

```
abstract class A {
    abstract function m():void;
}
```

## Static classes

```
static class MyNamespace {
    public static const VALUE:Number = 10.5;
}
```

## Final classes

```
final class A {}

class B extends A {} // ERROR!
```

## Override

```
class A {
    function m() {}
}

class B extends A {
    override function m() { trace("B!") }
}
```

## Final method

```
class A {
    final function m() {}
}

class B extends A {
    override function m() { trace("B!") } // ERROR!
}
```

## Super

```
class A {
    function A() { trace("A!") }

    function m() { trace("A.m!") }
}

class B extends A {
    function B() { super(); trace("B!") }

    override function m() { super.m(); trace("B.m!") }
}
```