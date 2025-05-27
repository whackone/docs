# Pixels and scale factor

Pixels are the main positioning unit used in the Display List.

## Scale factor

In the Display List, all the pixel positions and sizes are influenced by the global scale factor.

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