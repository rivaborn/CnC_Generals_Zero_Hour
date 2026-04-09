# Generals/Code/Tools/GUIEdit/Include/GUIEdit.h

## Purpose
Header file defining the GUIEdit class, which provides an editor framework for manipulating GameWindow objects and managing UI layouts.

## Responsibilities
- Manages editor modes (edit, test, drag, resize, etc.)
- Handles window selection, creation, and manipulation
- Provides grid snapping and visibility controls
- Manages status bar and toolbar UI elements
- Handles file I/O for saving/loading layouts

## Key Types
- **EditMode (Enum)**: Editor operation modes (edit, test, drag, resize variants)
- **StatusPart (Enum)**: Status bar segment identifiers
- **CursorType (Enum)**: Mouse cursor types for different operations
- **WindowSelectionEntry (Struct)**: Linked list node for selected windows
- **GUIEdit (Class)**: Main editor class managing UI layout editing

## Key Functions
### `init()`
- Purpose: Initialize editor data structures
- Calls: Not inferable

### `update()`
- Purpose: Process editor updates
- Calls: Not inferable

### `newWindow()`
- Purpose: Create a new GameWindow instance
- Calls: `clipCreationParamsToParent()`, `notifyNewWindow()`

### `computeResizeLocation()`
- Purpose: Calculate new window size/position during resize operations
- Calls: Not inferable

### `menuSave()`
- Purpose: Handle save operation
- Calls: `saveData()`, `setUnsaved()`

## Globals
- **TheEditor (GUIEdit*)**: Singleton instance of the editor

## Dependencies
- `GameClient/GameWindow.h`
- `GameClient/WindowLayout.h`
- `GameClient/GameWindowManager.h`
- `GUIEditColor.h`
- `Common/AsciiString.h`
- Windows.h, stdio.h
