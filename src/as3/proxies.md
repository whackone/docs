# Proxies

`jet_proxy` methods may be defined in a class or interface to allow overriding language behavior.

> **Note**: Unlike with Adobe ActionScript 3, a `Proxy` class does not need to be extended for overriding language behavior.

## jet_proxy::keys()

Must return an `Iterator.<T>` object. Used by the `for..in` statement.

```
jet_proxy function keys():Iterator.<T> {
    //
}
```

## jet_proxy::values()

Must return an `Iterator.<T>` object. Used by the `for each..in` statement.

```
jet_proxy function values():Iterator.<T> {
    //
}
```

## jet_proxy::get()

```
jet_proxy function get(key:K):V {
    //
}
```

## jet_proxy::set()

```
jet_proxy function set(key:K, value:V):void {
    //
}
```

## jet_proxy::delete()

```
jet_proxy function delete(key:K):Boolean {
    //
}
```

## jet_proxy::has()

Overrides the behavior of the `in` operator.

```
jet_proxy function has(key:K):Boolean {
    //
}
```

## jet_proxy::getAttribute()

Overrides the behavior of the `.@k` accessor.

```
jet_proxy function getAttribute(key:K):V {
    //
}
```

## jet_proxy::setAttribute()

Overrides the behavior of the `.@k = v` accessor.

```
jet_proxy function setAttribute(key:K, value:V):void {
    //
}
```

## jet_proxy::deleteAttribute()

Overrides the behavior of the `delete (...).@k` accessor.

```
jet_proxy function deleteAttribute(key:K):Boolean {
    //
}
```