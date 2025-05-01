# Points

A point is a 1/72nd of an inch.

## Scale factor

In the display list, the size of points is affected by the point scale factor (`Stage#pointScaleFactor`).

```
// Handle point scale change
stage.on("pointScaleChange", function() {
    //
});

stage.pointScaleFactor = 10; 
```