# Namespaces

ActionScript 3 uses three-dimensional property names: a property consists of a namespace and a local name.

## Private access

You can use ActionScript namespaces to privatize definitions across class fields and access them from any package as long as the used namespace is in scope:

```
// my_lib_internals.as
package my.lib {
    /**
     * @private
     */
    public namespace my_lib_internals = "http://my.lib/internals";
}

// Atom.as
package my.lib.atoms {
    import my.lib.*;

    public class Atom {
        /**
         * @private
         */
        my_lib_internals var x:Number = 10;
    }
}

// consumer.as
import my.lib.*;
import my.lib.atoms.*;

const atom = new Atom();
trace(atom.my_lib_internals::x);
```