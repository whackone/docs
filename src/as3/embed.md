# Embed

The `Embed()` expression may be used for embedding static media into the program.

```
// embedding text
const text:String = Embed("data.txt");

// embedding images
const arrow:ByteArray = Embed("arrow.svg");
```

> **Note**: in Adobe Flash Player, traditionally an `Embed` meta-data was used in definitions in order to embed static files; this is not the case in the Jet engine.

## MIME type

The file MIME type may be specified to force how the media is going to be processed:

```
const text:ByteArray = Embed("data.txt", type="application/octet-stream");
```