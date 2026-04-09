# Generals/Code/Tools/GUIEdit/Include/EditWindow.h

## Purpose
Header for the `EditWindow` class, which manages the GUI editing tool's main window and rendering.

## Responsibilities
- Manages the edit window singleton
- Handles window creation, rendering, and input events
- Provides drawing utilities (lines, rectangles, images)
- Supports drag-and-drop, resizing, and selection of GUI controls

## Key Types
- **EditWindow (Class)**: Main edit window singleton for GUI editing tool

## Key Functions
### `init`
- Purpose: Initialize the edit window singleton
- Calls: `registerEditWindowClass`

### `draw`
- Purpose: Draw the edit window and its contents
- Calls: `drawGrid`, `drawSeeThruOutlines`, `drawHiddenOutlines`, `drawUIFeedback`

### `mouseEvent`
- Purpose: Handle mouse events (clicks, moves, etc.)
- Calls: `handleResizeAvailable`, `inCornerTolerance`, `inLineTolerance`

### `editProc`
- Purpose: Windows callback for handling messages
- Calls: None (static, no `this` pointer)

## Globals
- **TheEditWindow (EditWindow*)**: Edit window singleton extern

## Dependencies
- `GUIEditColor.h`, `GameClient/Image.h`, `GameClient/GameWindow.h`, `WW3D2/AssetMgr.h`, `WW3D2/Render2D.h`
- Windows API (`windows.h`)
- `ICoord2D`, `IRegion2D`, `RGBColorReal`, `GameWindow`
