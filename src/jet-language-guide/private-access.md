# Private access

You can use Jet namespaces to privatize definitions across class fields and access them from any package as long as the used namespace is in scope:

```
// my_lib_internals.jet
package my.lib {
    public namespace my_lib_internals = "http://my.lib/internals";
}

// Atom.jet
package my.lib.atoms {
    import my.lib.*;

    public class Atom {
        my_lib_internals var x:Number = 10;
    }
}

// consumer.jet
import my.lib.*;
import my.lib.atoms.*;

const atom = new Atom();
trace(atom.my_lib_internals::x);
```