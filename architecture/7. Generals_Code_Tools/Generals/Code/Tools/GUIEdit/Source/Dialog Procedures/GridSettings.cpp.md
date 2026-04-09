# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/GridSettings.cpp

## Purpose
Handles the grid settings dialog for the GUI editor, allowing users to configure grid visibility, resolution, snap behavior, and color.

## Responsibilities
- Manages grid settings dialog initialization and input
- Handles color selection and preview rendering
- Updates editor grid properties on dialog acceptance
- Processes user commands (OK/Cancel/Close)

## Key Types
- `RGBColorInt` (struct): Represents a color with RGBA components

## Key Functions
### `initGridSettings`
- Purpose: Initializes dialog controls with current editor grid settings
- Calls: `SetDlgItemInt`, `CheckDlgButton`, `TheEditor->getGridResolution`, `TheEditor->isGridVisible`, `TheEditor->isGridSnapOn`, `TheEditor->getGridColor`

### `GridSettingsDialogProc`
- Purpose: Windows dialog procedure for handling grid settings UI messages
- Calls: `initGridSettings`, `SetDlgItemInt`, `CheckDlgButton`, `TheEditor->setGridResolution`, `TheEditor->setGridVisible`, `TheEditor->setGridSnap`, `TheEditor->setGridColor`, `SelectColor`, `CreateSolidBrush`, `DeleteObject`, `EndDialog`

## Globals
- `gridColor` (RGBColorInt): Stores the current grid color during dialog session

## Dependencies
- Windows API (`windows.h`)
- `RGBColorInt` from `BaseType.h`
- `TheEditor` (global editor instance)
- `Resource.h` for dialog control IDs
- `EditWindow.h` and `GUIEdit.h` for editor interface
