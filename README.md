# __name__

One sentence that says what __name__ does.

```lus nocheck
local __name__ = require("https://atmosp.here/__line__/__name__.lus")
print(__name__.greet("Ada"))
```

## Development

```sh
lus test
atmos check
```

A signed commit on `main` publishes to `unstable`. `atmos publish` tags and pushes a release for Lus __line__. The version starts below 1.0.0, so it publishes to `unstable` until `@version` reaches 1.0.0.
