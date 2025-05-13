# Interfaces

Interfaces are non opaque types that may be implemented by classes through the `implements` clause.

```
interface I {
    //
    public function m() : void;

    //
    public function get x() : Number;
    public function set x(value);
}

interface Ia extends I {}
```

All interface methods must omit the body.