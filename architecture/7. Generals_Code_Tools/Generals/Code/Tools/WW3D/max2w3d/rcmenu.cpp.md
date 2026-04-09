# Generals/Code/Tools/WW3D/max2w3d/rcmenu.cpp

## Purpose
Manages the right-click context menu for 3D model export options in the Max2W3D tool.

## Responsibilities
- Initializes the right-click menu with export options
- Handles menu selection callbacks
- Toggles hierarchy and geometry export flags

## Key Types
- RCMenuClass: Manages right-click menu behavior
- W3DAppData2Struct: Stores export settings for 3D nodes

## Key Functions
### RCMenuClass::Init
- Purpose: Creates the right-click menu with export options
- Calls: InterfacePtr->PickNode, W3DAppData2Struct::Get_App_Data

### RCMenuClass::Selected
- Purpose: Handles menu selection events
- Calls: Toggle_Hierarchy, Toggle_Geometry

### RCMenuClass::Toggle_Hierarchy
- Purpose: Toggles hierarchy export flag
- Calls: W3DAppData2Struct::Get_App_Data, Enable_Export_Transform

### RCMenuClass::Toggle_Geometry
- Purpose: Toggles geometry export flag
- Calls: W3DAppData2Struct::Get_App_Data, Enable_Export_Geometry

## Globals
- TheRCMenu (RCMenuClass): Singleton instance of the right-click menu manager

## Dependencies
- rcmenu.h, w3dutil.h, util.h
- INode, RightClickMenuManager, W3DAppData2Struct (external)
