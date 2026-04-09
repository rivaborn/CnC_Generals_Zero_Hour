# Generals/Code/Tools/WorldBuilder/src/EditGroup.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for editing script groups in WorldBuilder, bridging the MFC-based UI layer with the game's scripting system. It serves as a thin adapter between user input and the underlying `ScriptGroup` logic.

## Cross-References
### Incoming
- Likely called from WorldBuilder's main UI framework when a user initiates group editing (e.g., via a menu or context action).

### Outgoing
- Directly interacts with `ScriptGroup` methods (`setName`, `setActive`, `setSubroutine`, `isActive`, `isSubroutine`, `getName`).
- Uses MFC classes (`CDialog`, `CButton`, `CEdit`) for UI rendering and event handling.

## Design Patterns
- **Adapter Pattern**: Converts MFC UI events into `ScriptGroup` method calls.
- **MVC (Model-View-Controller)**: The dialog acts as the view/controller, while `ScriptGroup` is the model.
- **Dependency Injection**: `ScriptGroup` is injected via constructor, decoupling the dialog from group creation.

*Not inferable*: No other patterns are clearly visible in the provided snippet.
