# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/LogicalListener.cpp

## Purpose
Manages logical audio listeners in the game's sound scene, handling their addition/removal and persistence.

## Responsibilities
- Manages logical listener lifecycle (add/remove from scene)
- Handles save/load functionality for listener properties
- Maintains timestamp tracking for listeners
- Provides factory registration for persistence

## Key Types
- LogicalListenerClass (Class): Core listener implementation with position, scale, and type mask
- (anonymous enum) (Enum): Chunk IDs for save/load (CHUNKID_VARIABLES, CHUNKID_BASE_CLASS)
- (anonymous enum) (Enum): Variable IDs for persistence (VARID_SCALE, VARID_POSITION, etc.)

## Key Functions
### Add_To_Scene
- Purpose: Adds listener to the active sound scene
- Calls: WWAudioClass::Get_Instance(), SoundSceneClass::Add_Logical_Listener

### Remove_From_Scene
- Purpose: Removes listener from the sound scene
- Calls: SoundSceneClass::Remove_Logical_Listener

### Save
- Purpose: Serializes listener state to chunk save
- Calls: SoundSceneObjClass::Save, WRITE_MICRO_CHUNK

### Load
- Purpose: Deserializes listener state from chunk load
- Calls: PersistClass::Load, READ_MICRO_CHUNK

## Globals
- _LogicalListenerPersistFactory (SimplePersistFactoryClass): Factory for LogicalListenerClass persistence
- m_OldestTimestamp (uint32): Tracks oldest listener timestamp
- m_NewestTimestamp (uint32): Tracks newest listener timestamp
- m_GlobalScale (float): Global scale factor for all listeners

## Dependencies
- LogicalListener.H, WWAudio.H, SoundScene.H, SoundChunkIDs.h, persistfactory.h
- WWAudioClass, SoundSceneClass, ChunkSaveClass, ChunkLoadClass, PersistClass
