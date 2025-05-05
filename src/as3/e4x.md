# ECMAScript for XML

ECMAScript for XML (E4X) comprises XML markup and XML data manipulation facilities.

## Markup

XML markup is directly used in ActionScript 3 for rendering reactive UI components.

```
package me.diantha.portfolio {
    public function Portfolio() {
        return (
            <>
                <j:HGroup xmlns:j="jet.components.**">
                    <!-- markup -->
                </j:HGroup>
            </>
        );
    }
}
```

XML namespaces are used for importing packages solely within the markup, either non-recursive (`q.f.*`) or recursive (`q.f.**`). It is additionally allowed to use lexical names and fully qualified names like `<jet.components.HGroup>` as long as the component name is in scope.

> **Note:** Unlike the E4X standard 2nd edition, markup does not result in `XML` or `XMLList` objects, but rather `ReactNode`; and there is support for `a` attributes without an attribute value, which equals `a={true}`.