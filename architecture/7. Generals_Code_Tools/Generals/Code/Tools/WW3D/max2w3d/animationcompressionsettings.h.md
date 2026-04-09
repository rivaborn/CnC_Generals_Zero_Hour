# Generals/Code/Tools/WW3D/max2w3d/animationcompressionsettings.h

## Purpose
Defines a dialog class for configuring animation compression settings in the Max2W3D exporter tool.

## Responsibilities
- Manages a modal dialog for animation compression options
- Handles user input for compression settings
- Applies settings to export options structure
- Initializes and saves dialog controls

## Key Types
- AnimationCompressionSettingsDialogClass (Class): Dialog handler for animation compression settings

## Key Functions
### AnimationCompressionSettingsDialogClass()
- Purpose: Constructor for the dialog class
- Calls: None

### Do_Modal()
- Purpose: Displays the modal dialog and processes user input
- Calls: Real_Message_Proc, Message_Proc

### Message_Proc()
- Purpose: Handles window messages for the dialog
- Calls: Initialize_Controls, Save_Settings

### Initialize_Controls()
- Purpose: Sets up dialog controls with current settings
- Calls: None

### Save_Settings()
- Purpose: Saves user-selected settings to the options structure
- Calls: None

## Globals
- None

## Dependencies
- windows.h, max.h, w3dutil.h
- Interface, HWND, W3dExportOptionsStruct (external types)
