# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundSceneObj.cpp

## Purpose
Manages sound objects in the game's audio scene, handling attachment to 3D objects, positioning, and persistence.

## Responsibilities
- Maintains a global list of sound objects with unique IDs
- Handles attachment of sounds to render objects (with optional bone attachment)
- Manages sound object positioning based on attached object transforms
- Implements save/load functionality for sound scene objects
- Provides frame update logic for dynamic sound positioning

## Key Types
- SoundSceneObjClass (Class): Base class for sound objects in the scene
- (anonymous enum) (Enum): Chunk IDs for save/load (CHUNKID_VARIABLES, CHUNKID_BASE_CLASS)
- (anonymous enum) (Enum): Variable IDs for save/load (VARID_ATTACHED_OBJ, VARID_ATTACHED_BONE, VARID_USER_DATA, VARID_USER_OBJ, VARID_ID)

## Key Functions
### SoundSceneObjClass()
- Purpose: Default constructor that initializes a new sound object with a unique ID
- Calls: Register_Sound_Object

### Attach_To_Object(RenderObjClass*, const char*)
- Purpose: Attaches sound to a render object at a specific bone
- Calls: Get_Bone_Index

### Attach_To_Object(RenderObjClass*, int)
- Purpose: Attaches sound to a render object at a specific bone index
- Calls: Apply_Auto_Position

### Apply_Auto_Position()
- Purpose: Updates sound transform based on attached object's transform
- Calls: Get_Bone_Transform, Get_Transform

### Save(ChunkSaveClass&)
- Purpose: Serializes sound object state for saving
- Calls: PersistClass::Save, WRITE_MICRO_CHUNK

### Load(ChunkLoadClass&)
- Purpose: Deserializes sound object state for loading
- Calls: PersistClass::Load, READ_MICRO_CHUNK, Set_ID, Request_Ref_Counted_Pointer_Remap

### Register_Sound_Object(SoundSceneObjClass*)
- Purpose: Adds a sound object to the global sorted list
- Calls: Find_Sound_Object

### Unregister_Sound_Object(SoundSceneObjClass*)
- Purpose: Removes a sound object from the global list
- Calls: Find_Sound_Object

### Find_Sound_Object(uint32, int*)
- Purpose: Binary search for a sound object by ID
- Calls: None

## Globals
- m_GlobalSoundList (DynamicVectorClass<SoundSceneObjClass*>): Global list of all sound objects
- m_NextAvailableID (uint32): Counter for generating unique sound object IDs
- m_IDListMutex (CriticalSectionClass): Mutex for thread-safe access to the global list

## Dependencies
- SoundSceneObj.h
- camera.h
- rendobj.h
- persistfactory.h
- SoundChunkIDs.h
- utils.h
- AudioCallbackClass (external)
- PersistClass (external)
- RefCountClass (external)
- SaveLoadSystemClass (external)
- CriticalSectionClass (external)
