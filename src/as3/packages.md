# Packages

ActionScript packages are used for organizing definitions, using left-to-right hierarchic names.

```
package { public var x = 10 }

package me.diantha { public var y = 15 }

// (top-level).x
x

import me.diantha.*;

// me.diantha.y
y
me.diantha.y
```

## Source tree

It is allowed to define how many items you wish in a source file. However, it is a good practice to keep the source tree the same as the package inheritance:

```
// <project>/src/me/someone/lib/SomeConst.as
package me.someone.lib {
    public const SomeConst:decimal = 10;
}
```

This source tree can be used to insert MXML files at the right package.