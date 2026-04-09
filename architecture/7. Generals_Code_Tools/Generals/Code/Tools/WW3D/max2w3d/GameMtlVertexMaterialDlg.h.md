# Generals/Code/Tools/WW3D/max2w3d/GameMtlVertexMaterialDlg.h

## Purpose
Defines a dialog class for managing vertex material properties in the Max2W3d tool.

## Responsibilities
- Manages UI controls for material properties (colors, opacity, shininess, etc.)
- Handles dialog messages and updates
- Provides methods to activate/deactivate and reload the dialog

## Key Types
- **GameMtl (Class)**: Base material class for the game.
- **GameMtlVertexMaterialDlg (Class)**: Dialog for vertex material properties.
- **(anonymous enum) (Enum)**: Defines MAX_STAGES = 2.
- **MAX_STAGES (Enum)**: Constant for maximum texture stages.

## Key Functions
### GameMtlVertexMaterialDlg::Dialog_Proc
- Purpose: Handles dialog messages.
- Calls: Not inferable.

### GameMtlVertexMaterialDlg::ActivateDlg
- Purpose: Activates/deactivates the dialog.
- Calls: Not inferable.

### GameMtlVertexMaterialDlg::ReloadDialog
- Purpose: Reloads the dialog content.
- Calls: Not inferable.

## Globals
- **AmbientSwatch (IColorSwatch*)**: Color swatch for ambient color.
- **DiffuseSwatch (IColorSwatch*)**: Color swatch for diffuse color.
- **SpecularSwatch (IColorSwatch*)**: Color swatch for specular color.
- **EmissiveSwatch (IColorSwatch*)**: Color swatch for emissive color.
- **OpacitySpin (ISpinnerControl*)**: Spinner for opacity value.
- **TranslucencySpin (ISpinnerControl*)**: Spinner for translucency value.
- **ShininessSpin (ISpinnerControl*)**: Spinner for shininess value.
- **UVChannelSpin (IS
