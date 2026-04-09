# Generals/Code/Tools/WW3D/max2w3d/GameMtlVertexMaterialDlg.cpp

## Purpose
Handles the UI dialog for vertex material properties in the Max2W3D exporter tool.

## Responsibilities
- Manages color swatches (ambient, diffuse, specular, emissive)
- Controls material property spinners (opacity, translucency, shininess)
- Handles UV channel assignments for texture stages
- Processes material mapping and PSX-specific settings
- Updates material properties when controls change

## Key Types
- `GameMtlVertexMaterialDlg` (Class): Main dialog class for vertex material properties
- `IColorSwatch` (Type): Color picker control interface
- `ISpinner` (Type): Numeric spinner control interface

## Key Functions
### `Dialog_Proc`
- Purpose: Windows message handler for the dialog
- Calls: `GetIColorSwatch`, `SetupFloatSpinner`, `SetupIntSpinner`, `TheMtl->Set_*`, `IParams->RollupMouseMessage`

### `ReloadDialog`
- Purpose: Refreshes all controls with current material values
- Calls: `TheMtl->Get_*`, `SetCheckBox`, `SendDlgItemMessage`, `SetWindowText`

### `ActivateDlg`
- Purpose: Activates/deactivates color swatches
- Calls: `AmbientSwatch->Activate`, etc.

## Globals
- `AmbientSwatch`, `DiffuseSwatch`, `SpecularSwatch`, `EmissiveSwatch` (`IColorSwatch*`): Color controls
- `OpacitySpin`, `TranslucencySpin`, `ShininessSpin` (`ISpinner*`): Material property spinners
- `UVChannelSpin[MAX_STAGES]` (`ISpinner*`): UV channel assignment spinners

## Dependencies
- `GameMtlVertexMaterialDlg.h`, `GameMtl.h`, `dllmain.h`, `resource.h`
- `IMtlParams`, `GameMtl` interfaces
- Windows API (`HWND`, `WPARAM`, `LPARAM`, etc.)
- `DebugPrint`, `assert` utilities
