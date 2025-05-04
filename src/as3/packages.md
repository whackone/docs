# Packages

ActionScript packages are used for organizing definitions.

```
package {
    // top-level package

    // globally visible `x`
    public var x = 10
}

package a {
    // `a` package.
}

package a.b {
    // `a.b` package, subpackage of `a`.

    public var y = 15
}

// lexical reference to top-level package's `x`
x

import a.b.*;

// lexical reference to `a.b.y`
y
// fully qualified reference to `a.b.y`
a.b.y
```