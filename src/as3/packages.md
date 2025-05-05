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