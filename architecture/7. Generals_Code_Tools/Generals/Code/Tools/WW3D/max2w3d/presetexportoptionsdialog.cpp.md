# Generals/Code/Tools/WW3D/max2w3d/presetexportoptionsdialog.cpp

## Purpose
Handles the UI dialog for preset export options in the Max2W3D tool, allowing users to configure export settings for W3D files.

## Responsibilities
- Manages dialog creation and message handling
- Updates export options based on user input
- Handles file browsing for hierarchy files
- Validates and enforces preset-specific settings
- Controls animation compression settings dialog

## Key Types
- **PresetExportOptionsDialogClass** (Class): Main dialog class handling export options UI
- **PANE_TYPE** (Enum): Identifies different settings panes (HLOD, animation, terrain, etc.)

## Key Functions
### Do_Modal
- Purpose: Displays the modal dialog and returns user selection
- Calls: DialogBoxParam

### Message_Proc
- Purpose: Handles dialog messages and dispatches to appropriate handlers
- Calls: Create_Settings_Panes, Initialize_Controls, Determine_Preset_Type

### Pane_Message_Proc
- Purpose: Processes messages for individual settings panes
- Calls: GetICustEdit, SetupIntSpinner, AnimationCompressionSettingsDialogClass::Do_Modal

### Save_Settings
- Purpose: Saves current settings and enforces preset-specific constraints
- Calls: memcmp, SetSaveRequiredFlag

## Globals
- **BROWSE_FILTER** (const char*): File filter string for W3D/WHT file browsing

## Dependencies
- presetexportoptionsdialog.h
- dllmain.h
- resource.h
- w3dexp.h
- animationcompressionsettings.h
- Max SDK interfaces (ICustEdit, ISpinnerControl)
- Windows API (DialogBoxParam, CreateDialogParam, etc.)
