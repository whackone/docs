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

### RT::arch

This configuration constant contains the target architecture identifier as part of the target triple; for example: `"x86_64"`, `"wasm32"`, `"aarch64"` or `"arm"`.

### RT::vendor

This configuration constant contains the target vendor identifier as part of the target triple.

### RT::os

This configuration constant contains the target operating system identifier as part of the target triple; for example: `"unknown"`, `"windows"`, `"ios"`, `"darwin"`, `"android"` or `"linux"`.