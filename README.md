# OXCE Custom UI Mods

Ruleset mods used to demonstrate and regression-test the custom GUI schema
framework developed for OpenXcom Extended 8.6.0.

The framework build targets OXCE 8.6.0 for XPiratez v0.1 compatibility. These
mods require an OXCE executable that includes the custom GUI schema framework;
stock OXCE 8.6.0 does not understand the `customUis` rules.

## Included mods

- `CustomUiSchemaTest` is the main interactive test suite. It covers Geoscape,
  Basescape, and Battlescape interfaces; controls; navigation; data providers;
  layout; colors; backgrounds; sorting; and scrolling.
- `CustomUiSchemaCompanion` provides the destination used by the suite's
  cross-mod navigation test.

Enable both mods to exercise every test. The companion is otherwise optional.

## Installation

Copy both mod directories into an OXCE mods directory:

```text
mods/
  CustomUiSchemaTest/
  CustomUiSchemaCompanion/
```

For a local framework test build, deploy them to:

```text
<framework-checkout>/build-custom-ui/bin/Release/standard/
```

See `CustomUiSchemaTest/README.md` for entry points and detailed test coverage.
