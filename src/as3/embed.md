# Embed

The `Embed()` expression may be used for embedding static media into the program.

Text

```
const text: String = Embed("data.txt");
```

Scalable vector graphics

```
const scalable: String = Embed("arrow.svg");
```

Portable network graphics

```
const portable: ByteArray = Embed("arrow.png");
```

> **Note**: In Flash Player, an `[Embed]` meta-data was used in definitions in order to embed static files; this is not the case with Jet engine.

## MIME type

The file MIME type may be specified to force how the media is going to be processed:

```
const text:ByteArray = Embed("data.txt", type="application/octet-stream");
```

MIME types representing binary files are incorporated as `ByteArray` objects.