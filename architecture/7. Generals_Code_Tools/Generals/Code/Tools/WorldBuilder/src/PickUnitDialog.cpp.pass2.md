# Generals/Code/Tools/WorldBuilder/src/PickUnitDialog.cpp - Enhanced Analysis

## Architectural Role
This file implements the unit selection UI for WorldBuilder, bridging the editor's MFC-based UI layer with the game's object system. It acts as a mediator between the editor's visual interface and the underlying `ThingFactory`/`ThingTemplate` hierarchy.

## Cross-References
### Incoming
- **WorldBuilderDoc.h**: Likely calls `PickUnitDialog` to populate unit lists during editor initialization.
- **WHeightMapEdit.h**: May invoke unit selection when placing objects in the world.

### Outgoing
- **ThingFactory**: Uses `TheThingFactory` to enumerate templates for the tree view.
- **ThingTemplate**: Relies on template properties (`getEditorSorting`, `getDefaultOwningSide`) for hierarchical sorting.
- **MFC Framework**: Extends `CDialog` and uses `CWnd` for UI rendering.

## Design Patterns
- **Composite**: The tree view hierarchy mirrors the `ThingTemplate` composition (side â sorting type â template).
- **Factory Method**: Delegates object creation to `TheThingFactory` via `firstTemplate()`.
- **Observer**: Handles `TVN_SELCHANGED` notifications to update selection state.

*Not inferable*: No clear use of Strategy or Decorator despite dynamic filtering.
