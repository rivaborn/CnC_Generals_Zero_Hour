# Generals/Code/Tools/GUIEdit/Include/GUIEditWindowManager.h

## Purpose
Manages GUI windows for the GUI edit tool, extending the W3D window manager with editing functionality.

## Responsibilities
- Manages window creation/destruction
- Handles clipboard operations (copy/cut/paste/duplicate)
- Maintains window hierarchy (parent/child relationships)
- Validates window names for uniqueness
- Tracks clipboard state for paste operations

## Key Types
- **GUIEditWindowManager (Class)**: Extends W3DGameWindowManager to provide GUI editing capabilities
- **GameWindow (Type)**: Base window type managed by this class

## Key Functions
### `winCreate`
- Purpose: Creates a new window with specified parameters
- Calls: Inherited from W3DGameWindowManager

### `duplicateSelected`
- Purpose: Duplicates selected windows into the clipboard
- Calls: `validateClipboardNames`, `duplicateWindow`

### `pasteClipboard`
- Purpose: Pastes clipboard contents into the window hierarchy
- Calls: `createClipboardDuplicate`

### `moveAheadOf`
- Purpose: Reorders windows in the hierarchy
- Calls: None visible

### `makeChildOf`
- Purpose: Establishes parent-child relationships between windows
- Calls: None visible

## Globals
- **TheGUIEditWindowManager (GUIEditWindowManager*)**: Singleton instance for editor use

## Dependencies
- `W3DGameWindowManager.h` (base class)
- `GameWindow` type (from W3D)
- Standard C++ types (Int, UnsignedInt, Bool)
