# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundSceneObj.cpp

## Purpose
Manages sound objects in the game's audio scene, handling attachment to 3D objects, positioning, and persistence.

## Responsibilities
- Maintains a global list of sound objects with unique IDs
- Handles attachment of sounds to render objects (bones or entire objects)
- Manages sound object positioning based on attached object transforms
- Implements save/load functionality for sound objects
- Provides frame update logic for sound positioning

## Key Types
- SoundSceneObjClass (Class): Base class for sound objects in the scene
- (anonymous enum) (Enum): Chunk IDs for save/load (CHUNKID_VARIABLES, CHUNKID_BASE_CLASS)
- (anonymous enum) (Enum): Variable IDs for save/load (VARID_ATTACHED_OBJ, VARID_ATTACHED_BONE, etc.)

## Key Functions
### SoundSceneObjClass()
- Purpose: Constructor that initializes sound object and registers it globally
- Calls: Register_Sound_Object

### Attach_To_Object()
- Purpose: Attaches sound to a render object (by bone name or index)
- Calls: Get_Bone_Index, Apply_Auto_Position

### Apply_Auto_Position()
- Purpose: Updates sound transform based on attached object's transform
- Calls: Get_Bone_Transform, Get_Transform, Set_Transform

### Save/Load()
- Purpose: Persistence methods for sound objects
- Calls: PersistClass::Save/Load, WRITE_MICRO_CHUNK/READ_MICRO_CHUNK

### Register_Sound_Object/Unregister_Sound_Object
- Purpose: Manages global sound object registry with thread-safe access
- Calls: Find_Sound_Object

### Find_Sound_Object()
- Purpose: Binary search for sound objects by ID in global list
- Calls: None

## Globals
- m_GlobalSoundList (DynamicVectorClass): Stores all active sound objects
- m_NextAvailableID (uint32): Tracks next available sound object ID
- m_IDListMutex (CriticalSectionClass): Protects access to global sound list

## Dependencies
- SoundSceneObj.h, camera.h, rendobj.h, persistfactory.h, SoundChunkIDs.h, utils.h
- AudioCallbackClass, PersistClass, RefCountClass, SaveLoadSystemClass
- Matrix3D, Vector3 classes for transform operations
