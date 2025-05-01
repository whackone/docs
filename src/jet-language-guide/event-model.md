# Event model

The native `EventEmitter` class is designated for dispatching and listening to events, and is the one used for implementing the event model in the display list API.

In addition, the `IEventEmitter` interface may be implemented instead of extending the `EventEmitter` class.

## Defining an event emitter

```
/** Event "play". */
[Event(name="play", type="Event")]
/**
 * The CN class.
 */
class CN extends EventEmitter {
    // constructor
    public function CN() {
        on("play", function() {
            trace("played");
        });
    }

    // a_method
    public function a_method() {
        emit(new Event("play"));
    }
}
```

## Emitting

The `EventEmitter#emit()` method is defined as follows:

```
public function emit.<E extends "event:object/this">(e:E) : Boolean {
    // code
}
```

## Adding listeners

The `EventEmitter#on()` method is roughly defined as follows:

```
public function on.<E extends "event:type/this">(
    type: E.name,
    listener: function(E.type):void,
) : void {
    // code
}
```