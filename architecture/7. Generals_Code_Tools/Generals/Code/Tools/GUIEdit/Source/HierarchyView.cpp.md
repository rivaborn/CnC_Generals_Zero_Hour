# Generals/Code/Tools/GUIEdit/Source/HierarchyView.cpp

## Purpose
Manages the hierarchy tree view for GUI editing, allowing manipulation of window relationships.

## Responsibilities
- Handles window drag-and-drop operations in the hierarchy
- Manages tree view control messages and rendering
- Maintains window parent-child relationships visually
- Provides context menus for hierarchy operations
- Tracks dialog position/size for persistence

## Key Types
- `HierarchyView` (Class): Main hierarchy view manager
- `dialogPos` (ICoord2D): Static tracking dialog position
- `dialogSize` (ICoord2D): Static tracking dialog size
- `TheHierarchyView` (HierarchyView*): Global singleton instance

## Key Functions
### `dialogProc`
- Purpose: Windows dialog procedure handling messages for the hierarchy view
- Calls: `getTreeHandle`, `getDragWindow`, `treePointToItem`, `getWindowFromItem`, `setDragTarget`, `validateDragDropOperation`, `setDragWindow`, `setDragTarget`, `setPopupTarget`, `clearSelections`, `selectWindow`

### `addWindow`
- Purpose: Adds a window to the hierarchy tree
- Calls: `findTreeEntry`, `addWindowToTree`, `InvalidateRect`

### `removeWindow`
- Purpose: Removes a window from the hierarchy tree
- Calls: `findTreeEntry`, `TreeView_DeleteItem`

### `moveWindowAheadOf`
- Purpose: Reorders windows in the hierarchy
- Calls: `removeWindow`, `findTreeEntry`, `TreeView_GetNextItem`, `TreeView_InsertItem`, `addWindowToTree`

### `validateDragDropOperation`
- Purpose: Validates if a drag-drop operation is logically allowed
- Calls: `winGetParent` (on GameWindow)

## Globals
- `dialogPos` (ICoord2D): Tracks dialog position between sessions
- `dialogSize` (ICoord2D): Tracks dialog size between sessions
- `TheHierarchyView` (HierarchyView*): Global singleton instance

## Dependencies
- Windows API (HWND, WM_*, etc.)
- Common controls (TreeView_*)
- `GameWindow` class (from GameClient)
- `GUIEdit` editor interface
- `Resource.h` for menu IDs
- Debug logging utilities
