# Classes

## Inheritance

By default a class extends `Object`. Use the `extends` clause for extending a specific class:

```
class B extends A {
    // block
}
```

## Constructor

By default the constructor is based in the base class's constructor and will initialize the instance with default property values.

Define a constructor for a class using its name in a function definition:

```
class A {
    public function A() {
        // constructor
    }
}
```