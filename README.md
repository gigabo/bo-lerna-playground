# Current failure:

```bash
$ npm run repro
```

### The issue:

The `prepublish` script for `packages/pkg-a` isn't run during bootstrap so the
tests fail in `packages/pkg-b`, since it uses `pkg-a` for testing.
