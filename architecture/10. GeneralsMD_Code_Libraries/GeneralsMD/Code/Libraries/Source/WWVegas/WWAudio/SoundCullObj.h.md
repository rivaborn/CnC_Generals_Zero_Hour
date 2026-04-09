# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundCullObj.h

## Purpose
Defines a sound culling object that wraps a SoundSceneObjClass for use with culling systems.

## Responsibilities
- Wraps SoundSceneObjClass for culling system integration
- Manages sound object's transform and bounding box
- Provides access to sound object properties
- Handles reference counting for the sound object

## Key Types
- **SoundCullObjClass (Class)**: Wraps a sound object for culling system use
- **SoundSceneObjClass (Pointer)**: The sound object being wrapped
- **Matrix3D (Member)**: Stores the object's transform
- **AABoxClass (Member)**: Stores the object's bounding box

## Key Functions
### SoundCullObjClass()
- Purpose: Default constructor initializing members
- Calls: None

### ~SoundCullObjClass()
- Purpose: Destructor releasing the sound object reference
- Calls: REF_PTR_RELEASE

### Get_Bounding_Box()
- Purpose: Returns the sound's bounding box based on drop-off radius
- Calls: Get_DropOff_Radius(), Get_Translation()

### Set_Transform()
- Purpose: Updates the object's transform and propagates to sound object
- Calls: Set_Cull_Box(), Get_Bounding_Box()

### Set_Sound_Obj()
- Purpose: Assigns a new sound object with reference counting
- Calls: REF_PTR_SET(), Get_Transform(), Set_Cull_Box()

## Globals
- None

## Dependencies
- soundsceneobj.h (SoundSceneObjClass)
- cullsys.h (CullableClass)
- refcount.h (REF_PTR_SET/RELEASE)
- mempool.h
- multilist.h (MultiListObjectClass)
