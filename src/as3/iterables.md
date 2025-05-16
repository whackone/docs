# Iterables

Any class that implements `Iterator.<T>` or defines `jet_proxy::keys()` and/or `jet_proxy::values()` may be iterated.

## jet_proxy usage

```
class A {
    //
    jet_proxy function keys() {
        for (var i = 0; i < 10; i++) {
            yield i;
        }
    }

    //
    jet_proxy function values() {
        for (var i = 0; i < 10; i++) {
            yield i;
        }
    }
}
```