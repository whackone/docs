# Conditional compilation

`NAMESPACE::CONSTANT` may match a set configuration constant.

```
NAMESPACE::CONSTANT {
    //
}

NAMESPACE::CONSTANT var x
```

Inline constants:

```
trace(NAMESPACE::CONSTANT)
```

## Pre-defined configuration constants

## RT::client

`RT::client` indicates whether the target environment is the client side.

## RT::server

`RT::server` indicates whether the target environment is the server side.