# Generals/Code/Tools/GUIEdit/Source/GUIEdit.cpp

## Purpose
This file implements the GUIEdit tool, a Windows-based editor for designing game UI layouts in the SAGE engine.

## Responsibilities
- Manages window/gadget creation, selection, and manipulation
- Handles file I/O for saving/loading UI layouts
- Provides grid snapping and safe positioning logic
- Maintains editor state (unsaved changes, visibility modes)
- Integrates with Windows dialogs for file operations

## Key Types
- GUIEdit (Class): Main editor class managing UI layout editing
- WindowSelectionEntry (Struct): Tracks selected windows in the editor
- IRegion2D (Struct): Defines 2D regions for selection operations

## Key Functions
### saveAsDialog
- Purpose: Opens Windows save dialog for .wnd files
- Calls: GetSaveFileName

### openDialog
- Purpose: Opens Windows open dialog for .wnd files
- Calls: GetOpenFileName

### setUnsaved
- Purpose: Updates window title and internal state for unsaved changes
- Calls: SetWindowText

### computeSafeSizeLocation
- Purpose: Calculates valid window position/size within parent or screen bounds
- Calls: None

### computeResizeLocation
- Purpose: Computes new window dimensions during resize operations
- Calls: computeSafeSizeLocation

### isNameDuplicate
- Purpose: Recursively checks for duplicate window names
- Calls: winGetChild, winGetNext

## Globals
- TheEditor (GUIEdit*): Singleton instance of the editor

## Dependencies
- Windows API (commctrl.h, windows.h)
- SAGE engine components (GameWindow, W3DDevice, etc.)
- GameClient UI gadgets (GadgetPushButton, etc.)
- File system abstractions (LocalFileSystem, ArchiveFileSystem)
