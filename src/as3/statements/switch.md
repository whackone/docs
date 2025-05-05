# Switch

The switch statement, as opposed to the standard, does not support fallthrough in cases.

```
switch (0) {
    case 0: {
        trace("zero");
    }
    case 1: {
        trace("one");
    }
}
```

The above prints "zero", not "zero" then "one".