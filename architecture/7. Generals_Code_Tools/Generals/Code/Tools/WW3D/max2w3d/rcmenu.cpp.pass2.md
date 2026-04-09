# Generals/Code/Tools/WW3D/max2w3d/rcmenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the right-click context menu system for the Max2W3D export tool, bridging the 3DS Max plugin interface with W3D-specific export functionality. It serves as the UI layer for controlling W3D export options during model preparation.

## Cross-References
### Incoming
- **3DS Max Plugin System**: Calls `RCMenuClass::Init` when right-click events occur in the viewport
- **W3D Export Pipeline**: Other export tools reference menu state through `W3DAppData2Struct`

### Outgoing
- **3DS Max SDK**: Uses `INode` picking and `RightClickMenuManager` for UI integration
- **W3D Data Model**: Modifies export flags via `W3DAppData2Struct` methods

## Design Patterns
- **Singleton Pattern**: `TheRCMenu` provides global access to menu state
- **Command Pattern**: Menu selections dispatch to toggle methods (`Toggle_Hierarchy`, `Toggle_Geometry`)
- **Adapter Pattern**: Translates 3DS Max UI events into W3D-specific export actions

*Not inferable*: No clear use of Observer or Factory patterns in this file.
