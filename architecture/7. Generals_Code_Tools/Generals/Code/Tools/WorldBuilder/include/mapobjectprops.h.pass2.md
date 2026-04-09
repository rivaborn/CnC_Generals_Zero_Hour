# Generals/Code/Tools/WorldBuilder/include/mapobjectprops.h - Enhanced Analysis

## Architectural Role
This header defines the `MapObjectProps` dialog class, which serves as the primary UI for editing map object properties in WorldBuilder. It bridges the gap between the visual editor and the underlying data model (Dict objects), enabling level designers to modify object attributes like position, health, and team affiliation.

## Cross-References
### Incoming
- **WorldBuilder UI**: Calls `MapObjectProps` constructor and methods like `updateTheUI()` to display and modify object properties.
- **Undo/Redo System**: Likely uses `ModifyObjectUndoable` for tracking changes to object properties.
- **Selection System**: Relies on `getSingleSelectedMapObject()` to retrieve the currently selected object.

### Outgoing
- **Dict System**: Reads/writes properties to/from `Dict` objects (e.g., `_DictToTeam`, `_DictToHealth`).
- **Slider Controls**: Interacts with `WBPopupSliderButton` for height/angle adjustments.
- **MapObject System**: Modifies properties of `MapObject` instances (e.g., `SetZOffset`, `SetAngle`).

## Design Patterns
- **Mediator**: `MapObjectProps` acts as a mediator between the UI and the underlying data model (`Dict` objects), centralizing property editing logic.
- **Observer**: The dialog updates its UI in response to changes in the selected object (e.g., `updateTheUI()`).
- **Command**: Uses `ModifyObjectUndoable` to encapsulate property changes as undoable actions, supporting the editor's undo/redo functionality.
