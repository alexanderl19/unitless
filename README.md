# unitless

This package provides the list of unitless CSS properties (accepts a number but is not a distance).
The list of properties that match this criteria is from `react-dom-bindings`'s [`isUnitlessNumber.js`](https://github.com/facebook/react/blob/c15579631ff4d387401d57d9006d849ca1d5cd71/packages/react-dom-bindings/src/shared/isUnitlessNumber.js).

As of 1.0.0, the list is from 18.2.0 of `react-dom-bindings`.

## Usage

`unitless` has two names exports: `unitlessNumbers` and `isUnitlessNumber`.

```ts
// unitlessNumbers is a Set
import { unitlessNumbers, isUnitlessNumber } from "unitless";

const property = "property";
const value = 1;

if (unitlessNumbers.has(property)) {
  return value;
} else {
  return value + "px";
}

// or more succinctly

return unitlessNumbers.has(property) ? value : value + "px";

// alternatively, using isUnitlessNumber

return isUnitlessNumber(property) ? value : value + "px";
```

## Versioning

Any breaking changes to the API will constitute a major version.

Updates to the properties list will constitute a minor version.

## Contributing

To install bun:

<https://bun.sh/docs/installation>

To install dependencies:

```bash
bun install
```

To build:

```bash
bun run build
```

## License

Copyright © 2023 Alexander Liu, Meta Platforms, Inc. and affiliates

MIT License
