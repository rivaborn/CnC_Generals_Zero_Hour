# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/htree.cpp

## Purpose
Manages hierarchical bone structures (h-trees) for 3D models, including loading, updating, and manipulating bone transforms.

## Responsibilities
- Load and parse W3D hierarchy data from files
- Update bone transforms for animations, blending, and combos
- Provide bone lookup and manipulation utilities
- Support bone capture/control for external transformations
- Create morphed/interpolated bone hierarchies

## Key Types
- **HTreeClass**: Manages a hierarchy of bones/pivots with transforms
- **PivotClass**: Represents a single bone with transform, parent, and visibility state
- **W3dHierarchyStruct/W3dPivotStruct**: W3D file format structures for hierarchy data

## Key Functions
### HTreeClass::Load_W3D
- Purpose: Load hierarchy data from a W3D file chunk
- Calls: `read_pivots`, `Free`

### HTreeClass::Anim_Update
- Purpose: Compute bone transforms for animated motion
- Calls: `Get_Transform`, animation motion functions

### HTreeClass::Blend_Update
- Purpose: Blend between two animation states for bone transforms
- Calls: Animation motion functions, `Get_Visibility`

### HTreeClass::Combo_Update
- Purpose: Combine multiple animations for bone transforms
- Calls: Animation motion functions, `Get_Visibility`

### HTreeClass::Get_Bone_Index
- Purpose: Find bone index by name
- Calls: None

### HTreeClass::Alter_Avatar_HTree
- Purpose: Special-case scaling for avatar bone structures
- Calls: None

## Globals
- None

## Dependencies
- Key includes: `htree.h`, `hanim.h`, `hcanim.h`, `wwmath.h`, `chunkio.h`, `w3d_file.h`
- External symbols: `MSGW3DNEWARRAY`, `W3DNEW`, `W3DNEWARRAY`, `WWMEMLOG`, `WWMath` functions
