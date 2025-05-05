# Points and scale factor

A point is a 1/72nd of an inch.

## Scale factor

In the display list, all the point units are affected by the global scale factor (`ScaleFactor#scale`).

```
scaleFactor.on("change", function() {
    //
});

scaleFactor.scale = 10; 
```