# Event model

The native `EventEmitter` class is designated for dispatching and listening to events, and is the one used for implementing the hierarchic event model in the display list API.

In addition, the `IEventEmitter` interface may be implemented instead of extending the `EventEmitter` class.

## Defining an event emitter

```
/** Event "play". */
[Event(name="play", type="Event")]
/** The CN class. */
class CN extends EventEmitter {
    // constructor
    public function CN() {
        this.on("play", function() { trace("played"); });
    }

    // a_method
    public function a_method() {
        this.emit(new Event("play"));
    }
}
```

## Defining event objects

Event constructors must always take the event type as the first argument; any other arguments may follow.

```
class SomeEvent extends Event {
    public function SomeEvent(type: String) {
        super(type);
    }
}
```

## Emitting

The `EventEmitter#emit()` method is defined as follows:

```
public function emit.<E extends this.MetaEvents::object>(e:E) : Boolean {
    // code
}
```

## Adding listeners

The `EventEmitter#on()` method is roughly defined as follows:

```
public function on.<E extends this.MetaEvents::type>(
    type: E.name,
    listener: function(E.type):void,
) : void {
    // code
}
```