# Generals/Code/Tools/WW3D/max2w3d/ExportAllDlg.h

## Purpose
Defines the `ExportAllDlg` class for handling export operations in the max2w3d tool.

## Responsibilities
- Manages the export dialog UI
- Handles directory selection and recursive export options
- Interfaces with the 3DS Max environment via `Interface`

## Key Types
- **ExportAllDlg (Class)**: Dialog for exporting assets from 3DS Max to W3D format.
- **Interface (Class)**: Reference to the 3DS Max interface (external).
- **(anonymous enum) (Enum)**: Contains the dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier.

## Key Functions
### ExportAllDlg()
- Purpose: Constructor for the export dialog.
- Calls: None.

### DoModal()
- Purpose: Displays the dialog modally.
- Calls: `DialogProc`.

### DialogProc()
- Purpose: Handles Windows messages for the dialog.
- Calls: `OnInitDialog`, `OnBrowse`, `OnOK`.

### OnInitDialog()
- Purpose: Initializes dialog controls.
- Calls: None.

### OnBrowse()
- Purpose: Opens a directory browser.
- Calls: None.

### OnOK()
- Purpose: Validates and processes export when OK is clicked.
- Calls: None.

## Globals
- **m_Directory (char[_MAX_PATH])**: Stores the selected export directory.
- **m_Recursive (BOOL)**: Flag for recursive export.
- **m_hWnd (HWND)**: Dialog window handle.
- **m_MaxInterface (Interface*)**: Reference to the 3DS Max interface.

## Dependencies
- `dllmain.h`, `resource.h`
- `Interface` class (external)
- Windows API (`HWND`, `WPARAM`, `LPARAM`,
