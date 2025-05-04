# Points

A point is a 1/72nd of an inch.

## Scale factor

In the display list, all point units are affected by the global scale factor (`GlobalScaleFactor#scale`).

```
// Handle global scale factor change
GlobalScaleFactor.instance.on("change", function() {
    //
});

GlobalScaleFactor.instance.scale = 10; 
```