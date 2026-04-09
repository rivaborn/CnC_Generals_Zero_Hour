# Generals/Code/Tools/WW3D/max2w3d/w3ddlg.cpp

## Purpose
Handles the W3D export options dialog for the Max2W3D tool, managing export settings for hierarchies, animations, and geometry.

## Responsibilities
- Manages the W3D export options dialog UI
- Handles user input for export settings
- Validates hierarchy file paths
- Initializes and manages open file dialogs
- Controls enable/disable states of UI elements based on export options

## Key Types
- `W3dOptionsDialogClass` (Class): Main dialog class handling export options
- `W3dExportOptionsStruct` (Struct): Contains export configuration options
- `OPENFILENAME` (Struct): Windows open file dialog structure

## Key Functions
### `W3dOptionsDialogClass::Dialog_Proc`
- Purpose: Handles Windows messages for the options dialog
- Calls: `Dialog_Init`, `Dialog_Ok`, `WHT_Export_Radio_Changed`, etc.

### `W3dOptionsDialogClass::Dialog_Init`
- Purpose: Initializes dialog controls with current export options
- Calls: `Enable_WHT_Export`, `Enable_WHA_Export`, `Enable_WTM_Export`

### `W3dOptionsDialogClass::Dialog_Ok`
- Purpose: Validates and saves user input from the dialog
- Calls: `SetSaveRequiredFlag`, `RawFileClass::Open`

### `_init_ofn`
- Purpose: Initializes the open file dialog structure
- Calls: None

## Globals
- `_OfnInited` (bool): Tracks if open file dialog is initialized
- `_HierarchyFileOFN` (OPENFILENAME): Open file dialog structure for hierarchy files

## Dependencies
- `w3ddlg.h`, `resource.h`, `dllmain.h`, `w3dexp.h`, `util.h`, `rawfile.h`, `string`, `units.h`, `presetexportoptionsdialog.h`
- Windows API (HWND, WPARAM, LPARAM, etc.)
- Max SDK interfaces (Interface, ExpInterface)
