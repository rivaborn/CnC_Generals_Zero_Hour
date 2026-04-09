# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundChunkIDs.h

## Purpose
Defines chunk IDs and class IDs for audio-related persist objects in the editor.

## Responsibilities
- Declares chunk IDs for various sound types (e.g., 3D sounds, filtered sounds).
- Defines class IDs for sound definitions.
- Provides globally-unique identifiers for save/load operations.

## Key Types
- (anonymous enum) (Enum): Chunk IDs for sound-related persist objects.
  - CHUNKID_SOUND_DEF (Enum): ID for sound definitions.
  - CHUNKID_AUDIBLE_SOUND (Enum): ID for audible sounds.
  - CHUNKID_FILTERED_SOUND (Enum): ID for filtered sounds.
  - CHUNKID_SOUND3D (Enum): ID for 3D sounds.
  - CHUNKID_PSEUDO_SOUND3D (Enum): ID for pseudo 3D sounds.
  - CHUNKID_STATIC_SAVELOAD (Enum): ID for static save/load objects.
  - CHUNKID_DYNAMIC_SAVELOAD (Enum): ID for dynamic save/load objects.
  - CHUNKID_LOGICALSOUND (Enum): ID for logical sounds.
  - CHUNKID_LOGICALLISTENER (Enum): ID for logical listeners.
- (anonymous enum) (Enum): Class IDs for sound definitions.
  - CLASSID_SOUND_DEF (Enum): Class ID for sound definitions.

## Key Functions
None.

## Globals
None.

## Dependencies
- `saveloadids.h`: For chunk ID definitions.
- `definitionclassids.h`: For class ID definitions.
