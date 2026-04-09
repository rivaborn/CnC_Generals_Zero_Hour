# Generals/Code/Libraries/Source/WWVegas/WWAudio/LogicalListener.cpp

## Purpose
Manages logical audio listeners in the game's sound scene, handling their lifecycle, persistence, and scene integration.

## Responsibilities
- Manages logical listener creation/destruction
- Handles scene integration (add/remove listeners)
- Implements save/load functionality for persistence
- Maintains listener properties (position, scale, type mask)

## Key Types
- LogicalListenerClass (Class): Core logical listener implementation
- (anonymous enum) (Enum): Chunk IDs for save/load
- (anonymous enum) (Enum): Variable IDs for save/load

## Key Functions
### LogicalListenerClass()
- Purpose: Default constructor initializing member variables
- Calls: None

### ~LogicalListenerClass()
- Purpose: Destructor
- Calls: None

### Add_To_Scene()
- Purpose: Adds listener to the sound scene's culling system
- Calls: WWAudioClass::Get_Instance(), SoundSceneClass::Add_Logical_Listener()

### Remove_From_Scene()
- Purpose: Removes listener from the sound scene
- Calls: SoundSceneClass::Remove_Logical_Listener()

### Save()
- Purpose: Serializes listener data to a chunk save stream
- Calls: SoundSceneObjClass::Save(), WRITE_MICRO_CHUNK()

### Load()
- Purpose: Deserializes listener data from a chunk load stream
- Calls: PersistClass::Load(), READ_MICRO_CHUNK()

## Globals
- _LogicalListenerPersistFactory (SimplePersistFactoryClass): Persistence factory for LogicalListenerClass
- m_OldestTimestamp (uint32): Tracks oldest timestamp
- m_NewestTimestamp (uint32): Tracks newest timestamp
- m_GlobalScale (float): Global scale factor

## Dependencies
- LogicalListener.H
- WWAudio.H
- SoundScene.H
- SoundChunkIDs.h
- persistfactory.h
- SoundSceneObjClass
- WWAudioClass
- ChunkSaveClass
- ChunkLoadClass
- PersistClass
