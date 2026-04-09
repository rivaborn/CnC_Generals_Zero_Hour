# Generals/Code/Tools/WW3D/max2w3d/skin.cpp

## Purpose
Handles skinning functionality for 3D models in the Max2W3D exporter tool, managing bone assignments and vertex influences.

## Responsibilities
- Manages skinning object and modifier classes
- Handles bone selection and assignment
- Provides UI dialogs for skinning parameters
- Processes vertex-bone influence data

## Key Types
- **SkinWSMObjectClassDesc (Class)**: Class descriptor for skinning objects
- **SkinModClassDesc (Class)**: Class descriptor for skinning modifiers
- **SkinWSMObjectCreateCallBack (Class)**: Handles object creation callbacks
- **SkinWSMObjectClass (Class)**: Main skinning object class
- **SkinModifierClass (Class)**: Skinning modifier class

## Key Functions
### Get_Tri_Object
- Purpose: Retrieves triangle object from object state
- Calls: None

### Bone_Distance
- Purpose: Calculates distance between bone and vertex
- Calls: None

### _sot_dialog_proc
- Purpose: Handles "supports objects of type" dialog messages
- Calls: None

### _skeleton_dialog_thunk
- Purpose: Handles skeleton parameter dialog messages
- Calls: SkinWSMObjectClass::Skeleton_Dialog_Proc

### _bone_influence_dialog_thunk
- Purpose: Handles bone influence dialog messages
- Calls: SkinModifierClass::Bone_Influence_Dialog_Proc

## Globals
- **_SkinWSMObjectDesc (SkinWSMObjectClassDesc)**: Skin object class descriptor
- **_SkinModDesc (SkinModClassDesc)**: Skin modifier class descriptor
- **_SkinCreateCB (SkinWSMObjectCreateCallBack)**: Object creation callback
- **SkinWSMObjectClass::SotHWND (HWND)**: Dialog window handle
- **SkinWSMObjectClass::SkeletonHWND (HWND)**: Skeleton dialog window handle
- **SkinWSMObjectClass::BoneListHWND (HWND)**: Bone list window handle

## Dependencies
- "skin.h", "dllmain.h", "max.h", "simpmod.h", "simpobj.h", "resource.h"
- "skindata.h", "bpick.h", "namedsel.h", "boneicon.h"
- Uses 3DS Max SDK classes (IObjParam, ICustButton, ISpinnerControl)
- Depends on W3D-specific types and constants
