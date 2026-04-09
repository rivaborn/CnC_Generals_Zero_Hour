# Generals/Code/Tools/GUIEdit/Include/GUIEdit.h - Enhanced Analysis

## Architectural Role
This header defines the core GUI editor framework, bridging the game's UI system (GameWindow/WindowLayout) with editor-specific functionality. It serves as the central interface for manipulating UI layouts during development, while maintaining tight coupling with the game's window management system.

## Cross-References
### Incoming
- `Generals/Code/Tools/GUIEdit/Src/GUIEdit.cpp` (implementation)
- `Generals/Code/Tools/GUIEdit/Src/Main.cpp` (editor entry point)
- `Generals/Code/GameClient/WindowLayout.cpp` (layout serialization)

### Outgoing
- Directly manipulates `GameWindow` hierarchy through `GameWindowManager`
- Uses `WindowLayout` for serialization/deserialization
- Depends on `GameClient` subsystem for rendering and input

## Design Patterns
- **Singleton Pattern**: `TheEditor` provides global access to editor instance
- **Composite Pattern**: Manages hierarchical `GameWindow` objects via linked list selection
- **Command Pattern**: Menu operations (`menuSave`, `menuOpen`) encapsulate UI actions

*Not inferable*: Factory pattern for window creation (e.g., `newPushButton`) not explicitly visible in header.
