# Generals/Code/Tools/GUIEdit/Source/GUIEditWindowManager.cpp

## Purpose
Manages GUI windows for the GUI edit tool, extending the W3D window manager with editing functionality.

## Responsibilities
- Manages clipboard operations for window editing
- Handles window creation/destruction with edit metadata
- Supports window hierarchy manipulation (parent/child relationships)
- Provides duplicate/paste functionality for windows
- Maintains selection state and child supervision

## Key Types
- `GUIEditWindowManager` (Class): Main window manager for the GUI editor
- `GameWindowEditData` (Struct): Edit-specific data attached to windows
- `WindowSelectionEntry` (Struct): Represents selected windows

## Key Functions
### `duplicateWindow`
- Purpose: Creates a duplicate of a source window with all its children
- Calls: `TheWindowManager->gogoGadget*`, `duplicateWindow` (recursive), `linkToClipboard`

### `makeChildOf`
- Purpose: Makes a target window a child of a parent window
- Calls: `unlinkChildWindow`, `linkWindow`, `addWindowToParent`, `TheHierarchyView->moveWindowChildOf`

### `moveAheadOf`
- Purpose: Repositions a window in the window hierarchy
- Calls: `unlinkChildWindow`, `unlinkWindow`, `insertWindowAheadOf`, `TheHierarchyView->moveWindowAheadOf`

### `cutSelectedToClipboard`
- Purpose: Cuts selected windows to clipboard and removes them from layout
- Calls: `resetClipboard`, `copySelectedToClipboard`, `TheEditor->deleteSelected`

## Globals
- `TheGUIEditWindowManager` (GUIEditWindowManager*): Singleton instance of the window manager

## Dependencies
- `W3DGameWindowManager` (base class)
- `GameWindow` (window system)
- `GUIEdit` (editor interface)
- `HierarchyView` (hierarchy visualization)
- `GadgetSlider` (slider widget)
- Windows API (`MessageBox`)
