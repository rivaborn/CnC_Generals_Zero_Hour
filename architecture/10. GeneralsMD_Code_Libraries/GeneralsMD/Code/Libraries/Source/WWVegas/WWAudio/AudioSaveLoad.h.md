# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AudioSaveLoad.h

## Purpose
Defines save/load subsystems for static and dynamic audio data in the game.

## Responsibilities
- Provides save/load functionality for static audio assets
- Provides save/load functionality for dynamic audio assets
- Implements chunk-based serialization for audio data
- Manages singleton instances for audio save/load systems

## Key Types
- StaticAudioSaveLoadClass (Class): handles saving/loading of static audio data
- DynamicAudioSaveLoadClass (Class): handles saving/loading of dynamic audio data

## Key Functions
### StaticAudioSaveLoadClass::Chunk_ID
- Purpose: Returns the chunk ID for static audio save/load
- Calls: None

### StaticAudioSaveLoadClass::Contains_Data
- Purpose: Checks if static audio data exists to save
- Calls: None

### StaticAudioSaveLoadClass::Save
- Purpose: Saves static audio data to a chunk
- Calls: None

### StaticAudioSaveLoadClass::Load
- Purpose: Loads static audio data from a chunk
- Calls: None

### DynamicAudioSaveLoadClass::Chunk_ID
- Purpose: Returns the chunk ID for dynamic audio save/load
- Calls: None

### DynamicAudioSaveLoadClass::Contains_Data
- Purpose: Checks if dynamic audio data exists to save
- Calls: None

### DynamicAudioSaveLoadClass::Save
- Purpose: Saves dynamic audio data to a chunk
- Calls: None

### DynamicAudioSaveLoadClass::Load
- Purpose: Loads dynamic audio data from a chunk
- Calls: None

## Globals
- _StaticAudioSaveLoadSubsystem (StaticAudioSaveLoadClass): Singleton instance for static audio save/load
- _DynamicAudioSaveLoadSubsystem (Dynamic
