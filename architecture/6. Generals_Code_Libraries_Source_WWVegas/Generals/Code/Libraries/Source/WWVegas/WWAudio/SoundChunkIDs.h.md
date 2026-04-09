# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundChunkIDs.h

## Purpose
Defines chunk IDs and class IDs for audio-related persist objects in the editor.

## Responsibilities
- Defines globally-unique chunk IDs for sound-related persist objects
- Defines class IDs for sound definitions in the editor
- Provides identifiers for the persist factory system

## Key Types
- (anonymous enum) (Enum): Chunk IDs for various sound types (e.g., audible, filtered, 3D sounds)
- CHUNKID_SOUND_DEF (Enum): Chunk ID for sound definitions
- CHUNKID_AUDIBLE_SOUND (Enum): Chunk ID for audible sounds
- CHUNKID_FILTERED_SOUND (Enum): Chunk ID for filtered sounds
- CHUNKID_SOUND3D (Enum): Chunk ID for 3D sounds
- CHUNKID_PSEUDO_SOUND3D (Enum): Chunk ID for pseudo 3D sounds
- CHUNKID_STATIC_SAVELOAD (Enum): Chunk ID for static save/load objects
- CHUNKID_DYNAMIC_SAVELOAD (Enum): Chunk ID for dynamic save/load objects
- CHUNKID_LOGICALSOUND (Enum): Chunk ID for logical sounds
- CHUNKID_LOGICALLISTENER (Enum): Chunk ID for logical listeners
- (anonymous enum) (Enum): Class IDs for sound definitions
- CLASSID_SOUND_DEF (Enum): Class ID for sound definitions

## Key Functions
None

## Globals
None

## Dependencies
- `saveloadids.h`: For chunk ID definitions
- `definitionclassids.h`: For class ID definitions
