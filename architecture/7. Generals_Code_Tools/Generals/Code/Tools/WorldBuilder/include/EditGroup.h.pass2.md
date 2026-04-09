# Generals/Code/Tools/WorldBuilder/include/EditGroup.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for editing script groups in WorldBuilder, bridging MFC dialog handling with the game's scripting system. It encapsulates the presentation logic for modifying `ScriptGroup` objects, which are likely used for mission scripting or level design.

## Cross-References
### Incoming
- **WorldBuilder UI modules**: Dialogs or views that need to edit script groups will instantiate `EditGroup`.
- **Scripting system**: The `ScriptGroup` class (referenced but not defined here) is the core data model being edited.

### Outgoing
- **MFC framework**: Uses `CDialog`, `CDataExchange`, and message maps for UI handling.
- **ScriptGroup implementation**: Interacts with the actual script group data structure (defined elsewhere).

## Design Patterns
- **MVC (Model-View-Controller)**: The `EditGroup` dialog acts as the view/controller for the `ScriptGroup` model.
- **Dependency Injection**: The `ScriptGroup` pointer is injected via constructor, decoupling UI from data.
- **Template Method**: `DoDataExchange` follows MFC's template method pattern for data binding.
