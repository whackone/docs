# Events

Events can be subscribed to and emitted through the `EventEmitter` class or the `IEventEmitter` interface.

```jet
package {
    import jet.events.*;

    /**
     * Event description.
     */
    [Event(name="event1", type="Event")]
    /**
     * N1
     */
    public class N1 extends EventEmitter {

        public function fire() {
            this.emit(new Event("event1"));
        }
    }
}

const obj = new N1();
obj.on("event1", function(e) {
    //
});
```

## Type inference

Type inference occurs when using events due to methods such as `on` containing a generic parameter, which in a rough sketch looks as follows:

```jet
public function on.<T extends this.events>(
    type: T.name, listener: function(T.type):(void,Boolean)
): void {
    // code
}
```

The `this.events` constraint causes `T` to be `{ name: String, type }` which is based in the inherited `[Event]` meta-data.

## Emitting events

The `emit()` method signature is defined by the Jet base as follows:

```jet
public function emit.<T extends this.event>(event: T): void {
    // code
}
```

The `this.event` constraint makes it so that the compiler will force the `Event` argument to be constructed correctly with the right constructor and right event type.