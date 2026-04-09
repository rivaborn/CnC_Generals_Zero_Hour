# Generals/Code/Tools/GUIEdit/Include/HierarchyView.h

## Purpose
Defines the `HierarchyView` class for manipulating window hierarchies in the GUI editor using a tree view control.

## Responsibilities
- Manages window hierarchy visualization via tree control
- Handles drag-and-drop operations for window reordering
- Provides tree item selection and navigation
- Maintains popup menu targets for context actions

## Key Types
- `HierarchyOption` (Enum): Specifies where to add a window (top/bottom)
- `HierarchyView` (Class): Main class for hierarchy manipulation
- `TheHierarchyView` (Global): Singleton instance of HierarchyView

## Key Functions
### `addWindowToTree`
- Purpose: Recursively adds a window and its children to the tree
- Calls: `findTreeEntry`, `addWindowToTree` (recursive)

### `dialogProc`
- Purpose: Handles Windows messages for the hierarchy dialog
- Calls: Not inferable (external Windows API)

### `validateDragDropOperation`
- Purpose: Checks if a drag-drop operation between windows is valid
- Calls: Not inferable

## Globals
- `TheHierarchyView` (HierarchyView*): Singleton instance of the hierarchy view

## Dependencies
- `<windows.h>`, `<commctrl.h>`: Windows API and common controls
- `"Lib/BaseType.h"`: Base types (Bool, Int, etc.)
- `"GameClient/GameWindow.h"`: GameWindow class definition
