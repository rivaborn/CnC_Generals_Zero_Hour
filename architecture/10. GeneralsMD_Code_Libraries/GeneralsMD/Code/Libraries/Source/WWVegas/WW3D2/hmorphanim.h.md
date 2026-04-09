# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmorphanim.h

## Purpose
Defines classes for handling morph-based animations, primarily for facial animation in the W3D engine.

## Responsibilities
- Manages morph animation data and channels
- Handles loading/saving morph animations from W3D files
- Provides frame interpolation and key management
- Supports multiple morphing channels (e.g., phonemes/expressions)

## Key Types
- **HMorphAnimClass (Class)**: Main morph animation class handling pose interpolation
- **TimeCodedMorphKeysClass (Class)**: Stores morph keys for animation channels
- **MorphKeyStruct (Struct)**: Contains morph frame and pose frame data
- **(anonymous enum) (Enum)**: Defines animation status codes (OK, LOAD_ERROR)

## Key Functions
### HMorphAnimClass::Load_W3D
- Purpose: Loads morph animation data from a W3D chunk
- Calls: read_channel, Resolve_Pivot_Channels

### TimeCodedMorphKeysClass::Get_Morph_Info
- Purpose: Retrieves interpolation data for a given morph frame
- Calls: get_index, binary_search_index

### HMorphAnimClass::Insert_Morph_Key
- Purpose: Adds a new morph key to the animation
- Calls: TimeCodedMorphKeysClass::Add_Key

## Globals
- None

## Dependencies
- "always.h", "hanim.h", "simplevec.h"
- HAnimClass, ChunkLoadClass, ChunkSaveClass, TextFileClass
- Vector3, Quaternion, Matrix3D, SimpleDynVecClass
