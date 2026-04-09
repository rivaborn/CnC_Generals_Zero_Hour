# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AudioSaveLoad.cpp

## Purpose
Handles saving and loading of audio-related data for the game's sound system.

## Responsibilities
- Manages static and dynamic audio scene persistence
- Serializes/deserializes sound scene data using chunk-based I/O
- Handles global audio variables (e.g., listener scale)
- Provides singleton instances for static/dynamic audio save/load operations

## Key Types
- `StaticAudioSaveLoadClass` (Class): Handles static audio scene persistence
- `DynamicAudioSaveLoadClass` (Class): Handles dynamic audio scene and variables persistence
- `CHUNKID_STATIC_SCENE` (Enum): Chunk ID for static scene data
- `CHUNKID_DYNAMIC_SCENE` (Enum): Chunk ID for dynamic scene data
- `CHUNKID_DYNAMIC_VARIABLES` (Enum): Chunk ID for dynamic variables
- `VARID_LOGICAL_LISTENER_GLOBAL_SCALE` (Enum): Variable ID for listener scale

## Key Functions
### `StaticAudioSaveLoadClass::Save`
- Purpose: Saves static sound scene data
- Calls: `SoundSceneClass::Save_Static`, `ChunkSaveClass::Begin_Chunk`, `ChunkSaveClass::End_Chunk`

### `StaticAudioSaveLoadClass::Load`
- Purpose: Loads static sound scene data
- Calls: `SoundSceneClass::Load_Static`, `ChunkLoadClass::Open_Chunk`, `ChunkLoadClass::Close_Chunk`

### `DynamicAudioSaveLoadClass::Save`
- Purpose: Saves dynamic sound scene and variables
- Calls: `SoundSceneClass::Save_Dynamic`, `ChunkSaveClass::Begin_Chunk`, `ChunkSaveClass::End_Chunk`, `WRITE_MICRO_CHUNK`

### `DynamicAudioSaveLoadClass::Load`
- Purpose: Loads dynamic sound scene and variables
- Calls: `SoundSceneClass::Load_Dynamic`, `ChunkLoadClass::Open_Chunk`, `ChunkLoadClass::Close_Chunk`, `ChunkLoadClass::Open_Micro_Chunk`, `ChunkLoadClass::Close_Micro_Chunk`, `LOAD_MICRO_CHUNK`

## Globals
- `_StaticAudioSaveLoadSubsystem` (StaticAudioSaveLoadClass): Singleton instance for static audio save/load
- `_DynamicAudioSaveLoadSubsystem` (DynamicAudioSaveLoadClass): Singleton instance for dynamic audio save/load

## Dependencies
- `audiosaveload.h`, `persist.h`, `persistfactory.h`, `definition.h`, `soundchunkids.h`, `chunkio.h`, `SoundScene.h`, `wwmemlog.h`
- `WWAudioClass`, `SoundSceneClass`,
