# Generals/Code/Tools/GUIEdit/Source/EditWindow.cpp

## Purpose
Main edit window implementation for the GUI editing tool in Command & Conquer Generals.

## Responsibilities
- Handles window creation, rendering, and event processing
- Manages UI feedback drawing (selection boxes, grids)
- Processes popup menus for creating new controls
- Coordinates with the editor's window management system

## Key Types
- `EditWindow` (Class): Main edit window class handling rendering and input
- `RGBColorReal` (Struct): Color representation with RGBA components
- `ICoord2D` (Struct): 2D coordinate point

## Key Functions
### `editProc`
- Purpose: Window procedure for handling Windows messages
- Calls: `updatePulse`, `mouseEvent`, `getPopupMenuClickPos`, `newWindow`, `deleteSelected`, `bringSelectedToTop`, `InitPropertiesDialog`

### `draw`
- Purpose: Renders the edit window and all contained UI elements
- Calls: `WW3D::Sync`, `WW3D::Begin_Render`, `TheWindowManager->winRepaint`, `drawUIFeedback`, `WW3D::End_Render`

### `openPopupMenu`
- Purpose: Displays context menu for creating new controls
- Calls: `LoadMenu`, `GetSubMenu`, `EnableMenuItem`, `TrackPopupMenuEx`

### `drawGrid`
- Purpose: Draws the background grid for alignment
- Calls: `TheDisplay->drawLine`

## Globals
- `TheEditWindow` (EditWindow*): Singleton instance of the edit window

## Dependencies
- Key includes: `EditWindow.h`, `GUIEdit.h`, `GameClient/Display.h`, `WW3D2/Render2D.h`
- External symbols: `TheEditor`, `TheWindowManager`, `TheDisplay`, `TheHierarchyView`, `WW3D`
