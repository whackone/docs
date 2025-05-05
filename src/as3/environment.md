# Environment and target

## Environment variables

Environment variables may be read from the project's `.env` file using the `import.meta.env.VAR_NAME` expression:

```
import.meta.env.FOO
```

## Target

### RT::client

This configuration constant indicates whether the compiler is targetting client-side code or not.

### RT::server

This configuration constant indicates whether the compiler is targetting server-side code or not.