# Generals/Code/Tools/WW3D/max2w3d/gmtldlg.cpp

## Purpose
Handles the material editor dialog for GameMtl in the 3DS Max plugin for W3D export.

## Responsibilities
- Manages UI dialogs for material properties
- Handles material parameter updates and validation
- Coordinates with 3DS Max material editor API
- Manages texture map assignments and animation parameters
- Provides PSX-specific material options

## Key Types
- GameMtlDlg (Class): Main dialog class for material editing
- IColorSwatch (Type): Color swatch control wrapper
- IntSpinner/FloatSpinner (Types): Spinner control wrappers

## Key Functions
### PanelProc
- Purpose: Main dialog message handler
- Calls: GetIColorSwatch, SetupIntSpinner, SetupFloatSpinner, UpdateMtlDisplay

### LoadDialog
- Purpose: Updates dialog controls with current material values
- Calls: InitColor, SetCheckBox, SetValue, UpdateTexmapDisplay

### UpdateMtlDisplay
- Purpose: Notifies 3DS Max that material parameters changed
- Calls: IParams->MtlChanged()

### PsxProc
- Purpose: Handles PSX-specific material options dialog
- Calls: SetMaskedAttribute, SetAttribute

## Globals
- None

## Dependencies
- Max.h, gport.h, hsv.h, bmmlib.h
- gmtldlg.h, gamemtl.h, gamemaps.h, dllmain.h, resource.h, w3d_file.h
- 3DS Max material editor API (IMtlParams)
- GameMtl class methods and attributes
