# Generals/Code/Tools/WW3D/max2w3d/presetexportoptionsdialog.h

## Purpose
Defines a dialog class for configuring W3D export options in the Max2W3d tool.

## Responsibilities
- Manages a modal dialog for export presets
- Handles different export pane types (HLOD, animation, terrain, etc.)
- Stores and restores export options
- Updates UI controls based on current settings

## Key Types
- **PresetExportOptionsDialogClass (Class)**: Main dialog class for export options.
- **(anonymous enum) (Enum)**: Defines pane types (PANE_HLOD, PANE_ANIM_HLOD, etc.).

## Key Functions
### PresetExportOptionsDialogClass()
- Purpose: Constructor for the dialog class.
- Calls: None visible.

### Do_Modal()
- Purpose: Displays the modal dialog.
- Calls: None visible.

### Set_Options()
- Purpose: Sets the export options to configure.
- Calls: None visible.

### Real_Message_Proc()
- Purpose: Static message handler for the dialog.
- Calls: None visible.

### Settings_Pane_Message_Proc()
- Purpose: Static message handler for settings panes.
- Calls: None visible.

### Message_Proc()
- Purpose: Handles dialog messages.
- Calls: None visible.

### Pane_Message_Proc()
- Purpose: Handles pane-specific messages.
- Calls: None visible.

### Settings_Message_Proc()
- Purpose: Handles settings pane messages.
- Calls: None visible.

### On_Command()
- Purpose: Handles command messages.
- Calls: None visible.

### Show_Settings_Pane()
- Purpose: Shows a specific settings pane.
- Calls: None visible.

### Create_Settings_Panes()
- Purpose: Creates all settings panes.
- Calls: None visible
