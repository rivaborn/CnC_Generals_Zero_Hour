# Generals/Code/Tools/WW3D/max2w3d/ExportAllDlg.cpp

## Purpose
Implements a dialog for exporting assets from 3DS Max to the W3D format, allowing users to select a directory and toggle recursive export.

## Responsibilities
- Manages the export dialog UI
- Handles directory selection via folder browser
- Validates user input before export
- Stores export settings (directory path, recursion flag)

## Key Types
- **ExportAllDlg (Class)**: Main dialog class handling export settings
- **Interface (Type)**: Reference to 3DS Max interface (external)

## Key Functions
### `DoModal`
- Purpose: Displays the export dialog and returns user choice
- Calls: `DialogBoxParam`, `_thunk_dialog_proc`

### `DialogProc`
- Purpose: Processes Windows messages for the dialog
- Calls: `OnInitDialog`, `OnOK`, `OnBrowse`

### `OnBrowse`
- Purpose: Opens folder browser and updates directory field
- Calls: `SHBrowseForFolder`, `SHGetPathFromIDList`

### `OnOK`
- Purpose: Validates user input and stores settings
- Calls: `GetWindowText`, `IsDlgButtonChecked`

## Globals
- **`_thunk_dialog_proc` (Function pointer)**: Dialog procedure thunk for Windows API

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `<shlobj.h>` (Windows Shell API)
- `Interface` class (3DS Max interface)
