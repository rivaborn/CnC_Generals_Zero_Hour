# Generals/Code/Libraries/Source/WWVegas/WW3D2/hmorphanim.h

## Purpose
Defines classes for handling morph animations, primarily for facial animation in the W3D engine.

## Responsibilities
- Manages morph animation data and channels
- Handles loading/saving morph animations from/to W3D format
- Provides access to animation frames, pivots, and morph keys
- Supports multiple morphing channels (e.g., phonemes, expressions)

## Key Types
- **HMorphAnimClass (Class)**: Main morph animation class handling facial morphs
- **TimeCodedMorphKeysClass (Class)**: Stores morph keys for each channel
- **MorphKeyStruct (Struct)**: Represents a morph key (morph frame + pose frame)
- **(anonymous enum) (Enum)**: Error codes (OK, LOAD_ERROR)

## Key Functions
### HMorphAnimClass::Load_W3D
- Purpose: Loads morph animation from W3D chunk
- Calls: read_channel, Resolve_Pivot_Channels

### HMorphAnimClass::Save_W3D
- Purpose: Saves morph animation to W3D chunk
- Calls: write_channel

### TimeCodedMorphKeysClass::Load_W3D
- Purpose: Loads morph keys from W3D chunk
- Calls: None

### TimeCodedMorphKeysClass::Get_Morph_Info
- Purpose: Retrieves morph interpolation data for a given frame
- Calls: get_index

## Globals
- None

## Dependencies
- Key includes: "always.h", "hanim.h", "simplevec.h"
- External symbols: ChunkLoadClass, ChunkSaveClass, TextFileClass, HAnimClass, Vector3, Quaternion, Matrix3D, SimpleDynVecClass
