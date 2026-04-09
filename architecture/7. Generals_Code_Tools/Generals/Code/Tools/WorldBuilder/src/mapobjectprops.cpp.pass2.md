# Generals/Code/Tools/WorldBuilder/src/mapobjectprops.cpp - Enhanced Analysis

## Architectural Role
This file implements the property editing UI for WorldBuilder, bridging the gap between the MFC-based editor UI and the game's data model (Dict-based properties). It handles serialization of object properties while maintaining undo/redo functionality.

## Cross-References
### Incoming
- **WorldBuilderDoc**: Calls `MapObjectProps` to display property dialogs
- **WBView**: Likely triggers property updates when objects are selected
- **PropEdit**: Used for advanced property editing (via `OnEditprop`)

### Outgoing
- **Dict**: Directly manipulates property dictionaries
- **ModifyObjectUndoable**: Creates undo actions for property changes
- **MapObject**: Queries object state and applies changes
- **NameKeyGenerator**: Converts internal keys to human-readable strings

## Design Patterns
- **Singleton**: `TheMapObjectProps` ensures only one property dialog exists
- **Command**: `ModifyObjectUndoable` encapsulates property changes as undoable actions
- **Observer**: UI updates react to selected object changes (via `updateTheUI`)

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
