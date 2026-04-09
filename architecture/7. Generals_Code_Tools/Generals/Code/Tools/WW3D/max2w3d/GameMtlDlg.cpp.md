# Generals/Code/Tools/WW3D/max2w3d/GameMtlDlg.cpp

## Purpose
Manages the material editor dialog for GameMtl (material) objects in 3DS Max plugin for W3D export.

## Responsibilities
- Creates and manages rollup dialogs for material properties
- Handles surface type, displacement maps, and pass count settings
- Updates material properties based on UI changes
- Manages pass-specific dialogs for multi-pass materials

## Key Types
- `GameMtlDlg` (Class): Main dialog manager for GameMtl materials
- `GameMtl` (Class): The material object being edited (external)
- `ISpinnerControl` (Class): MAX spinner control interface (external)

## Key Functions
### `GameMtlDlg::Build_Dialog`
- Purpose: Creates all rollup dialog pages for the material editor
- Calls: `IParams->AddRollupPage`, `new GameMtlPassDlg`, `ReloadDialog`

### `GameMtlDlg::ReloadDialog`
- Purpose: Refreshes all dialog controls with current material values
- Calls: `SendMessage`, `SetWindowText`, `PassDialog[i]->ReloadDialog`

### `GameMtlDlg::Set_Pass_Count_Dialog`
- Purpose: Handles pass count modification dialog
- Calls: `DialogBoxParam`, `new GameMtlPassDlg`, `ReloadDialog`

### `DisplacementMapProc`
- Purpose: Handles displacement map dialog messages
- Calls: `SetupIntSpinner`, `SetDlgItemInt`, `PostMessage`

### `SurfaceTypeProc`
- Purpose: Handles surface type dialog messages
- Calls: `SendDlgItemMessage`, `SetupIntSpinner`, `GetISpinner`

## Globals
- `_Pass_Index_To_Flag` (int[]): Maps pass indices to rollup flags

## Dependencies
- MAX SDK headers (`Max.h`, `gport.h`, `hsv.h`, `bmmlib.h`)
- Project headers (`GameMtlDlg.h`, `GameMtl.h`, `GameMtlPassDlg.h`, `dllmain.h`, `resource.h`, `w3d_file.h`)
- External symbols: `AppInstance`, `GameMaterialClassID`, `PS2GameMaterialClassID`, `Get_String`
