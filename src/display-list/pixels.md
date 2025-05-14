# Pixels and scale factor

Pixels are the main positioning unit used in the Jet engine.

## Scale factor

In the display list, all the pixel positions and sizes are affected by the global scale factor.

```
scaleFactor.on("change", function() {
    //
});

scaleFactor.scale = 10; 
```