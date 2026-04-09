# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanim.cpp

## Purpose
Manages hierarchical animation (HAnim) combinations, including motion blending and pivot weight mapping for skeletal animations.

## Responsibilities
- Handles HAnimComboDataClass and HAnimComboClass for animation management
- Manages pivot weight maps for bone influence control
- Provides motion blending and weight normalization
- Supports reference counting for shared animation data

## Key Types
- **NamedPivotMapClass** (Class): Maps named bones to weights for animation blending
- **HAnimComboDataClass** (Class): Stores animation motion, pivot map, frame data, and weight
- **HAnimComboClass** (Class): Manages a collection of HAnimComboDataClass instances
- **PivotMapClass** (Class): Base class for pivot weight mapping (external)
- **HAnimClass** (Class): Base animation class (external)

## Key Functions
### `NamedPivotMapClass::Update_Pivot_Map`
- Purpose: Configures pivot weights based on bone presence in a hierarchy tree
- Calls: `HTreeClass::Get_Bone_Index`, `HTreeClass::Num_Pivots`

### `HAnimComboDataClass::Build_Active_Pivot_Map`
- Purpose: Creates a pivot map marking which bones have animation data
- Calls: `HAnimClass::Get_Num_Pivots`, `HAnimClass::Is_Node_Motion_Present`

### `HAnimComboClass::Normalize_Weights`
- Purpose: Ensures animation weights sum to 1 for proper blending
- Calls: `HAnimComboDataClass` accessors, `PivotMapClass` operations

## Globals
- **None**

## Dependencies
- `hanim.h`, `assetmgr.h`, `htree.h`, `motchan.h`, `chunkio.h`, `w3d_file.h`, `wwdebug.h`
- `NamedPivotMapClass`, `HAnimComboDataClass`, `HAnimComboClass`, `PivotMapClass`, `HAnimClass` (external)
- `WWMath`, `WWMATH_EPSILON` (math utilities)
