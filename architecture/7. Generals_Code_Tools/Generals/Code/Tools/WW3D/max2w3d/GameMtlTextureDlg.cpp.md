# Generals/Code/Tools/WW3D/max2w3d/GameMtlTextureDlg.cpp

## Purpose
Handles the texture configuration dialog for GameMtl materials in the Max2W3d exporter tool.

## Responsibilities
- Manages UI controls for texture stages (frame count, rate, animation, hints)
- Handles texture file selection and display settings
- Synchronizes UI state with material properties
- Supports both PC and PS2 shader types with appropriate UI restrictions

## Key Types
- `GameMtlTextureDlg` (Class): Main dialog class for texture configuration
- `GameMtl` (Class): Material class being configured
- `BitmapInfo` (Struct): Texture file information
- `BitmapTex` (Class): Texture map class

## Key Functions
### `Dialog_Proc`
- Purpose: Windows message handler for the dialog
- Calls: `SetupIntSpinner`, `SetupFloatSpinner`, `GetICustButton`, `TheMtl->Set_Texture_*`, `Update_Texture_Buttons`, `Enable_Stage`

### `ReloadDialog`
- Purpose: Refreshes all UI controls with current material values
- Calls: `TheMtl->Get_Texture_*`, `SendDlgItemMessage`, `SetCheckBox`, `Update_Texture_Buttons`, `Enable_Stage`

### `Enable_Stage`
- Purpose: Enables/disables UI controls for a specific texture stage
- Calls: `TheMtl->Set_Texture_Enable`, `EnableWindow`

### `Update_Texture_Buttons`
- Purpose: Updates texture button labels with current filenames
- Calls: `TheMtl->Get_Texture`, `SplitPathFile`, `SetDlgItemText`

## Globals
- `Stage0FramesSpin` (ISpinner*): Frame count spinner for stage 0
- `Stage1FramesSpin` (ISpinner*): Frame count spinner for stage 1
- `Stage0RateSpin` (ISpinner*): Frame rate spinner for stage 0
- `Stage1RateSpin` (ISpinner*): Frame rate spinner for stage 1
- Various `ICustButton*` pointers for UI controls

## Dependencies
- `GameMtlTextureDlg.h`, `GameMtl.h`, `dllmain.h`, `resource.h`
- `<Max.h>`, `<bmmlib.h>`, `<stdmat.h>`
- `GameMtlFormClass`, `W3dMaterialClass`, `IParams`, `TheManager`
