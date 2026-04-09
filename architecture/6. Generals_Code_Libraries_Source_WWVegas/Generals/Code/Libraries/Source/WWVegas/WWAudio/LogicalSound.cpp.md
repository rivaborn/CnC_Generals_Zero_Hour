# Generals/Code/Libraries/Source/WWVegas/WWAudio/LogicalSound.cpp

## Purpose
Manages logical sound objects in the game's audio system, handling positioning, scene integration, and notification logic.

## Responsibilities
- Manages sound scene integration (add/remove)
- Handles sound position updates and auto-positioning
- Controls notification timing and listener management
- Implements save/load persistence for sound properties

## Key Types
- LogicalSoundClass (Class): Core logical sound object with scene management and notification logic
- (anonymous enum) (Enum): Chunk IDs for save/load (CHUNKID_VARIABLES, CHUNKID_BASE_CLASS)
- (anonymous enum) (Enum): Variable IDs for persistence (VARID_DROP_OFF_RADIUS, VARID_IS_SINGLE_SHOT, etc.)

## Key Functions
### Add_To_Scene
- Purpose: Adds the sound to the active sound scene
- Calls: WWAudioClass::Get_Instance(), SoundSceneClass::Add_Logical_Sound

### Remove_From_Scene
- Purpose: Removes the sound from the sound scene
- Calls: SoundSceneClass::Remove_Logical_Sound

### Allow_Notify
- Purpose: Determines if a notification should be allowed based on timing
- Calls: None

### On_Frame_Update
- Purpose: Updates sound position and processes frame updates
- Calls: Apply_Auto_Position(), SoundSceneObjClass::On_Frame_Update

### Save/Load
- Purpose: Persistence handling for sound properties
- Calls: SoundSceneObjClass::Save/Load, ChunkSaveClass/ChunkLoadClass methods

## Globals
- _LogicalSoundPersistFactory (SimplePersistFactoryClass): Persistence factory for LogicalSoundClass

## Dependencies
- LogicalSound.H, WWAudio.H, SoundScene.H, SoundChunkIDs.h, persistfactory.h
- ChunkSaveClass, ChunkLoadClass, SoundSceneClass, WWAudioClass, SoundSceneObjClass
