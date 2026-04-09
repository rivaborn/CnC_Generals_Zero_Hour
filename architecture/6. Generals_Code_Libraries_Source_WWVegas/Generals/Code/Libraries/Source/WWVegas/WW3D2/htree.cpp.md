# Generals/Code/Libraries/Source/WWVegas/WW3D2/htree.cpp

## Purpose
Manages hierarchical bone structures (h-trees) for 3D models, including loading, updating, and querying bone transforms.

## Responsibilities
- Load and parse W3D hierarchy data from files
- Update bone transforms for animations (base, blend, combo)
- Query bone indices, names, and parent relationships
- Support bone capture/control for manual transformations
- Create morphed/interpolated h-trees

## Key Types
- **HTreeClass**: Main class managing bone hierarchy
- **PivotClass**: Represents individual bones with transforms
- **W3dHierarchyStruct**: Header data for W3D hierarchy files
- **W3dPivotStruct**: Pivot data structure from W3D files

## Key Functions
### HTreeClass::Load_W3D
- Purpose: Loads hierarchy data from a W3D file chunk
- Calls: `read_pivots`, `Free`

### HTreeClass::Combo_Update
- Purpose: Computes bone transforms using weighted animation combos
- Calls: `Get_Motion`, `Get_Frame`, `Get_Pivot_Weight_Map`, `Get_Weight`, `Release_Ref`, `Get_Translation`, `Get_Orientation`, `Fast_Slerp`, `Slerp_`

### HTreeClass::Get_Bone_Index
- Purpose: Finds bone index by name
- Calls: None

### HTreeClass::Scale
- Purpose: Scales all pivot translations by a factor
- Calls: `Get_Translation`, `Set_Translation`

### HTreeClass::Create_Morphed
- Purpose: Creates a new h-tree by morphing between multiple source trees
- Calls: None

## Globals
- None

## Dependencies
- Key includes: `htree.h`, `hanim.h`, `hcanim.h`, `wwmath.h`, `chunkio.h`, `w3d_file.h`, `wwmemlog.h`, `hrawanim.h`, `motchan.h`
- External symbols: `MSGW3DNEWARRAY`, `W3DNEW`, `W3DNEWARRAY`, `WWMEMLOG`, `WWMath::Fabs`, `Vector3::Lerp`, `Matrix3D::Multiply`, `Build_Matrix3D`, `Fast_Slerp`, `Slerp_`
