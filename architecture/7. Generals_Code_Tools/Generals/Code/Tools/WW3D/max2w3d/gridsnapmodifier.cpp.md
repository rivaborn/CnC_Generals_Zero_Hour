# Generals/Code/Tools/WW3D/max2w3d/gridsnapmodifier.cpp

## Purpose
Implements a 3D Studio Max modifier plugin for snapping vertices to a grid, intended to reduce cracks between adjacent meshes in game levels.

## Responsibilities
- Defines `GridSnapModifierClass` for vertex grid snapping
- Implements `GridSnapDeformerClass` for geometry transformation
- Provides parameter block for grid dimension control
- Registers modifier via `ClassDesc2` for Max plugin system

## Key Types
- **GridSnapModifierClass (Class)**: Main modifier class inheriting from `SimpleMod2`
- **GridSnapDeformerClass (Class)**: Deformer implementation for vertex snapping logic
- **GridSnapModifierClassDesc (Class)**: Plugin descriptor for Max integration
- **(anonymous enum)**: Parameter block IDs
- **GSM_PARAMS (Enum)**: Parameter block identifier
- **GSM_PARAM_GRIDDIMENSION (Enum)**: Grid dimension parameter ID

## Key Functions
### Get_Grid_Snap_Modifier_Desc
- Purpose: Returns the plugin descriptor for Max integration
- Calls: None

### GridSnapModifierClass::GetDeformer
- Purpose: Creates and configures the deformer with current parameters
- Calls: `pblock2->GetValue`, `deformer.Set_Grid_Dimension`, `deformer.Set_Matrices`

### GridSnapDeformerClass::Map
- Purpose: Snaps vertex positions to the grid
- Calls: None (uses basic math operations)

## Globals
- **_GridSnapModifierDesc (GridSnapModifierClassDesc)**: Plugin descriptor instance
- **_GridSnapParamBlockDesc (ParamBlockDesc2)**: Parameter block definition

## Dependencies
- Max SDK headers (`Max.h`, `iparamb2.h`)
- Internal headers (`simpmod.h`, `dllmain.h`)
- Uses `SimpleMod2`, `Deformer`, `ClassDesc2`, `IParamBlock2` from Max SDK
