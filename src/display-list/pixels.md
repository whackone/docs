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

Note that the `stage.width` and `.height` properties are always unscaled pixels. To obtain the stage's resolution influenced by the scale factor, use the following snippet:

```
stage.width / scaleFactor.scale
stage.height / scaleFactor.scale
```

For instance, if `stage.width == 10` and `scaleFactor.scale == 10`, then `stage.width / scaleFactor.scale == 1` (`0` for the left side; `1` for the right side).