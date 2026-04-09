# Generals/Code/Libraries/Source/WWVegas/WWAudio/AudioSaveLoad.cpp

## Purpose
Handles saving and loading of audio-related data for the game's sound system.

## Responsibilities
- Manages static and dynamic audio scene persistence
- Defines chunk IDs for audio data serialization
- Implements save/load functionality for audio subsystems
- Handles logical listener global scale persistence

## Key Types
- StaticAudioSaveLoadClass (Class): handles static audio scene persistence
- DynamicAudioSaveLoadClass (Class): handles dynamic audio scene and variables persistence
- (anonymous enum) (Enum): defines chunk IDs for audio data
- (anonymous enum) (Enum): defines variable IDs for dynamic audio data

## Key Functions
### StaticAudioSaveLoadClass::Save
- Purpose: Saves static audio scene data
- Calls: SoundSceneClass::Save_Static, ChunkSaveClass methods

### StaticAudioSaveLoadClass::Load
- Purpose: Loads static audio scene data
- Calls: SoundSceneClass::Load_Static, ChunkLoadClass methods

### DynamicAudioSaveLoadClass::Save
- Purpose: Saves dynamic audio scene and variables
- Calls: SoundSceneClass::Save_Dynamic, LogicalListenerClass::Get_Global_Scale, ChunkSaveClass methods

### DynamicAudioSaveLoadClass::Load
- Purpose: Loads dynamic audio scene and variables
- Calls: SoundSceneClass::Load_Dynamic, LogicalListenerClass::Set_Global_Scale, ChunkLoadClass methods

## Globals
- _StaticAudioSaveLoadSubsystem (StaticAudioSaveLoadClass): global instance for static audio persistence
- _DynamicAudioSaveLoadSubsystem (DynamicAudioSaveLoadClass): global instance for dynamic audio persistence

## Dependencies
- audiosaveload.h, persist.h, persistfactory.h, definition.h, soundchunkids.h, chunkio.h, SoundScene.h, wwmemlog.h
- WWAudioClass, SoundSceneClass, LogicalListenerClass, ChunkSaveClass, ChunkLoadClass
