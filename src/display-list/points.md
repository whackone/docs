# Points and scale factor

A point is a 1/72nd of an inch.

## Scale factor

In the display list, all the points are affected by the global scale factor (`ScaleFactor#scale`).

```
// Handle scale factor change
scaleFactor.on("change", function() {
    //
});

scaleFactor.scale = 10; 
```