# Custom UI Schema Test Suite

This is an interactive test mod for the ruleset-driven custom GUI framework
added to the OXCE 8.6.0 branch. It is intentionally compatible with any master
mod (`master: "*"`) so it can be exercised with X-Com, TFTD, or XPiratez.

Enable both **Custom UI Schema Test Suite** and **Custom UI Cross-Mod Companion**
from the Mods screen. The companion is only needed for the **Other mod**
navigation test.

## Entry points

- **Geoscape:** `MOD UIS` -> click `GUI Schema Test: Main`
- **Basescape:** `MOD UIS` -> `GUI Schema Test: Basescape`
- **Battlescape:** Extended Links -> Custom UIs, or right-click the
  Links/layer button, then click `GUI Schema Test: Battlescape`

Interface names in the picker open directly when clicked. The **Open** button
and normal confirm key remain available as keyboard/controller alternatives.

## Coverage

- screen dimensions, all nine anchors, signed offsets, scaling, backgrounds,
  drawing-order overlap, and left/center/right text alignment;
- label, button, toggle, text input, search, numeric input, dropdown, list, and
  table widgets;
- large/word-wrapped text, per-widget colors, nested `[color]` tags, and
  default/hover/focused/selected button states;
- bool/int/string values, interpolation, placeholders, maximum input length,
  numeric clamping, steps, large steps, wrapping, arrows, and mouse wheel;
- scalar and text/value dropdown options;
- research, items, bases, soldiers, and crafts providers; current/all base
  scope, zero-item filtering, search, fixed/dynamic sort, descending sort,
  selectable/non-selectable tables, selection bindings, and selection actions;
- named and literal close actions, push/replace custom navigation, native UI
  navigation, same-mod and cross-mod targets;
- every controlled script operation: `getInt`, `getText`, `setInt`, `setText`,
  `setWidgetText`, one/all `refresh`, `close`, `open`, and `openNative`;
- Geoscape, Basescape, and Battlescape discovery and runtime contexts.

The schema deliberately has no standalone image widget, container, z-index,
responsive reflow, hidden/disabled state, or persistence API, so those are not
claimed as test coverage.
