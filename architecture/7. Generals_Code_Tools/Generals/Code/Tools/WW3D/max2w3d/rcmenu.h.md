# Generals/Code/Tools/WW3D/max2w3d/rcmenu.h

## Purpose
Defines the right-click menu class for the W3D utility plugin in 3ds Max.

## Responsibilities
- Manages right-click context menu for W3D utility
- Handles menu initialization and selection events
- Provides toggle functionality for hierarchy and geometry visibility
- Maintains reference to selected node and utility instance

## Key Types
- **RCMenuClass (Class)**: Right-click menu implementation for W3D utility
- **W3DUtilityClass (Class)**: Reference to the main utility class (external)
- **(anonymous enum) (Enum)**: Menu item identifiers (separator, toggles, node info)

## Key Functions
### RCMenuClass::Init
- Purpose: Initializes the right-click menu with manager, window handle, and mouse position
- Calls: Not inferable

### RCMenuClass::Selected
- Purpose: Handles menu item selection events
- Calls: Not inferable

### RCMenuClass::Toggle_Hierarchy
- Purpose: Toggles hierarchy visibility for a given node
- Calls: Not inferable

### RCMenuClass::Toggle_Geometry
- Purpose: Toggles geometry visibility for a given node
- Calls: Not inferable

## Globals
- **TheRCMenu (RCMenuClass)**: Global instance of the right-click menu

## Dependencies
- Max.h, dllmain.h, resource.h, istdplug.h
- RightClickMenu (base class)
- INode, Interface (3ds Max SDK types)
