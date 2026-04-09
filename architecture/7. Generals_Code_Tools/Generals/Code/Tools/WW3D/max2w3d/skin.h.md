# Generals/Code/Tools/WW3D/max2w3d/skin.h

## Purpose
Defines classes for a 3D skin modifier plugin for Max, enabling bone-based deformation and vertex weighting.

## Responsibilities
- Declares `SkinWSMObjectClass` for managing space warp objects and bone selection
- Declares `SkinModifierClass` for handling vertex skinning and bone influence
- Provides UI and serialization support for the skinning workflow

## Key Types
- **SkinWSMObjectClass (Class)**: Manages bone selection and space warp object behavior
- **SkinModifierClass (Class)**: Handles vertex skinning and bone influence calculations
- **BONE_SEL_MODE_* (Enum)**: Bone selection modes (none, add, remove, add many, remove many)
- **OBJ_REF/NODE_REF (Enum)**: Reference indices for modifier
- **OBJECT_SEL_LEVEL/VERTEX_SEL_LEVEL (Enum)**: Sub-object selection levels
- **NUM_BONES_CHUNK/SEL_LEVEL_CHUNK (Enum)**: Chunk IDs for serialization

## Key Functions
### Get_Skin_Obj_Desc
- Purpose: Returns ClassDesc for SkinWSMObjectClass
- Calls: None

### Get_Skin_Mod_Desc
- Purpose: Returns ClassDesc for SkinModifierClass
- Calls: None

## Globals
- **SotHWND, SkeletonHWND, BoneListHWND (HWND)**: Static UI window handles
- **InterfacePtr (IObjParam*)**: Cached Max interface pointer
- **AddBonesButton, RemoveBonesButton (ICustButton*)**: UI buttons for bone management
- **BasePoseSpin (ISpinnerControl*)**: Spinner control for base pose frame

## Dependencies
- `<Max.h>`: Max SDK headers
- `"simpmod.h"`, `"simpobj.h"`: Simple modifier/object base classes
- `"bpick.h"`: Bone picker interface
- `"namedsel.h"`: Named selection sets
- `"w3d_file.h"`: W3D file format definitions
