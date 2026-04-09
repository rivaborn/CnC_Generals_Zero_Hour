# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanim.cpp

## Purpose
Manages hierarchical animation (HAnim) combinations, including motion blending and pivot weight mapping for skeletal animation.

## Responsibilities
- Handles HAnimComboClass and HAnimComboDataClass for animation blending
- Manages pivot weight maps for per-bone influence control
- Provides frame and weight interpolation for animations
- Supports shared and non-shared animation data references
- Normalizes animation weights for proper blending

## Key Types
- **HAnimComboClass (Class)**: Manages a collection of animations and their blending parameters
- **HAnimComboDataClass (Class)**: Stores individual animation data (motion, pivot map, frame, weight)
- **NamedPivotMapClass (Class)**: Maps named bones to weights for animation influence
- **PivotMapClass (Class)**: Base class for pivot weight maps (referenced but not defined here)

## Key Functions
### `NamedPivotMapClass::Update_Pivot_Map`
- Purpose: Configures pivot weights based on bone names in an HTree
- Calls: `Tree->Num_Pivots()`, `Tree->Get_Bone_Index()`

### `HAnimComboDataClass::Build_Active_Pivot_Map`
- Purpose: Creates a pivot map marking which bones have animation data
- Calls: `HAnim->Get_Num_Pivots()`, `HAnim->Is_Node_Motion_Present()`

### `HAnimComboClass::Normalize_Weights`
- Purpose: Ensures animation weights sum to 1 for proper blending
- Calls: `Peek_Motion()`, `Peek_Pivot_Weight_Map()`, `Get_Weight()`

## Globals
- **DEFINE_AUTO_POOL(HAnimComboDataClass,256)**: Memory pool for HAnimComboDataClass instances

## Dependencies
- `hanim.h`, `assetmgr.h`, `htree.h`, `motchan.h`, `chunkio.h`, `w3d_file.h`, `wwdebug.h`
- `WWMath`, `WWMATH_EPSILON`, `NEW_REF`, `WWASSERT`
