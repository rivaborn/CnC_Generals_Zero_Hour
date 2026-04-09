# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/LogicalSound.cpp

## Purpose
Manages logical sound objects in the game's audio system, handling their lifecycle, scene integration, and serialization.

## Responsibilities
- Manages logical sound objects in the audio scene
- Handles sound position updates and culling
- Implements notification throttling for sound events
- Provides persistence (save/load) for logical sounds
- Integrates with the sound scene system

## Key Types
- LogicalSoundClass (Class): Core class managing logical sound behavior
- (anonymous enum) (Enum): Chunk IDs for serialization
- (anonymous enum) (Enum): Variable IDs for micro-chunks in serialization

## Key Functions
### Add_To_Scene
- Purpose: Adds the sound to the audio scene for culling
- Calls: WWAudioClass::Get_Instance(), SoundSceneClass::Add_Logical_Sound

### Remove_From_Scene
- Purpose: Removes the sound from the audio scene
- Calls: SoundSceneClass::Remove_Logical_Sound

### Allow_Notify
- Purpose: Determines if a notification should be allowed based on timing
- Calls: None

### On_Frame_Update
- Purpose: Updates the sound's position and processes frame updates
- Calls: Apply_Auto_Position(), SoundSceneObjClass::On_Frame_Update

### Save/Load
- Purpose: Serializes/deserializes the logical sound object
- Calls: SoundSceneObjClass::Save/Load, ChunkSaveClass/ChunkLoadClass methods

## Globals
- _LogicalSoundPersistFactory (SimplePersistFactoryClass): Persistence factory for LogicalSoundClass

## Dependencies
- LogicalSound.H, WWAudio.H, SoundScene.H, SoundChunkIDs.h, persistfactory.h
- ChunkSaveClass, ChunkLoadClass, SoundSceneClass, WWAudioClass, SoundSceneObjClass
