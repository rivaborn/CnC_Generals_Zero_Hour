# Generals/Code/Tools/WW3D/max2w3d/animationcompressionsettings.cpp

## Purpose
Handles the UI dialog for animation compression settings in the Max2W3D tool.

## Responsibilities
- Manages a modal dialog for animation compression options
- Initializes and saves compression settings
- Handles Windows message loop for the dialog
- Validates and bounds-checks user input

## Key Types
- **AnimationCompressionSettingsDialogClass (Class)**: Manages the dialog and settings
- **Interface (Type)**: 3DS Max interface (external)
- **HWND (Type)**: Windows handle (external)

## Key Functions
### AnimationCompressionSettingsDialogClass()
- Purpose: Constructor initializes dialog state
- Calls: None

### Do_Modal()
- Purpose: Displays the dialog and returns user response
- Calls: `DialogBoxParam`

### Message_Proc()
- Purpose: Handles Windows messages for the dialog
- Calls: `Initialize_Controls`, `Save_Settings`, `EndDialog`

### Initialize_Controls()
- Purpose: Populates dialog controls with current settings
- Calls: `SetCheckBox`, `ComboBox_AddString`, `ComboBox_SetCurSel`, `SetDlgItemText`

### Save_Settings()
- Purpose: Reads user input and updates settings
- Calls: `ComboBox_GetCurSel`, `IsDlgButtonChecked`, `GetDlgItemText`, `atof`

## Globals
- **AppInstance (HINSTANCE)**: Windows application instance (external)
- **IDD_ANIMATION_COMPRESSION (int)**: Dialog resource ID (external)

## Dependencies
- `animationcompressionsettings.h`
- `dllmain.h`
- `resource.h`
- `w3dexp.h`
- Windows API (`windows.h` implied)
- 3DS Max SDK (via `Interface` type)
