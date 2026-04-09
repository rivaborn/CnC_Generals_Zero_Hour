# Generals/Code/Tools/GUIEdit/Include/Properties.h - Enhanced Analysis

## Architectural Role
This header defines the core data structures and interface for the GUIEdit tool's property dialog system, which is used to edit UI control properties in the game. It serves as the bridge between the tool's UI and the underlying GameWindow system, enabling runtime modification of control states, colors, and images.

## Cross-References
### Incoming
- `ScriptProperties.h` (WorldBuilder) references `GetStateInfo` and dialog handling functions, indicating GUIEdit's property system is reused across tools.

### Outgoing
- Directly interacts with `GameWindow` (GameClient) for window property management.
- Uses `Image` and `Color` types from the rendering subsystem (W3D).
- Depends on Win32 API for dialog management (HWND, messages).

## Design Patterns
- **State Pattern**: `StateIdentifier` enum and `ImageAndColorInfo` struct explicitly model UI control states (enabled/disabled/hilite) and their visual representations.
- **Data Transfer Object (DTO)**: `ImageAndColorInfo` acts as a DTO to serialize/deserialize control properties between the editor and runtime.
- **Registry Pattern**: Global functions like `GetStateInfo` and `StoreImageAndColor` imply a centralized registry for state management.
