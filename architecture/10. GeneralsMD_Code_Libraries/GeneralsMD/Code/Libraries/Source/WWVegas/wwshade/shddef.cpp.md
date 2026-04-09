# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddef.cpp

## Purpose
Defines the `ShdDefClass` for handling surface material properties in the game engine.

## Responsibilities
- Manages surface material definitions (e.g., metal, water, tiberium).
- Serializes/deserializes material data via chunk I/O.
- Provides accessors for material properties.

## Key Types
- `ShdDefClass` (Class): Represents a surface material definition with name and type.
- `(anonymous enum)` (Enum): Chunk IDs for serialization.
- `CHUNKID_VARIABLES` (Enum): Chunk ID for material variables.
- `VARID_NAME` (Enum): Micro-chunk ID for material name.
- `VARID_SURFACETYPE` (Enum): Micro-chunk ID for surface type.

## Key Functions
### `ShdDefClass::Save`
- Purpose: Serializes the material definition to a chunk.
- Calls: `Begin_Chunk`, `Save_Variables`, `End_Chunk`.

### `ShdDefClass::Load`
- Purpose: Deserializes the material definition from a chunk.
- Calls: `Open_Chunk`, `Cur_Chunk_ID`, `Load_Variables`, `Close_Chunk`.

### `ShdDefClass::Save_Variables`
- Purpose: Writes material variables to micro-chunks.
- Calls: `WRITE_MICRO_CHUNK_WWSTRING`, `WRITE_MICRO_CHUNK`.

### `ShdDefClass::Load_Variables`
- Purpose: Reads material variables from micro-chunks.
- Calls: `Open_Micro_Chunk`, `Cur_Micro_Chunk_ID`, `Close_Micro_Chunk`.

## Globals
None.

## Dependencies
- `shddef.h`, `chunkio.h`, `w3d_file.h`
- `ChunkSaveClass`, `ChunkLoadClass`, `ENUM_PARAM` macro.
