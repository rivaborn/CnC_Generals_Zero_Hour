# Generals/Code/Tools/WW3D/max2w3d/rcmenu.h - Enhanced Analysis

## Architectural Role
This file defines the right-click context menu system for the W3D export plugin in 3ds Max, bridging the Max SDK's UI framework with the W3D utility's functionality. It serves as the user interaction layer for node visibility toggles during model preparation.

## Cross-References
### Incoming
- `max2w3d.cpp` (likely calls `RCMenuClass::Init` and `Selected` during plugin initialization and right-click handling)
- `W3DUtilityClass` (uses `Toggle_Hierarchy`/`Toggle_Geometry` for node state management)

### Outgoing
- 3ds Max SDK (`RightClickMenu`, `INode`, `Interface`) for menu management and node operations
- `resource.h` for menu item IDs (implied by `MENU_*` enum)

## Design Patterns
- **Singleton**: `TheRCMenu` provides global access to the right-click menu instance
- **Observer**: Menu selection events trigger actions on the `W3DUtilityClass` (event-driven UI pattern)
- **Bridge**: Decouples menu presentation from node manipulation logic via `UtilityPtr` reference

*Not inferable: No clear use of Command pattern for menu actions (toggles are direct method calls).*
