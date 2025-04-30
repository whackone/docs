# Points

A point is a 1/72nd of an inch.

## Scale factor

In the display list, the size of a point is affected by the point scale factor (`Stage#pointScale`).

```
// Handle point scale change
stage.on("pointscale", function() {
    //
});

stage.pointScale = 10; 
```