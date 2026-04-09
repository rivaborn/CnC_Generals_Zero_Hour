# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpdiff.cpp

## Purpose
Implements the bump-diffuse shader class for the SAGE engine, handling texture and bump map rendering with configurable lighting parameters.

## Responsibilities
- Defines shader parameters (textures, colors, bumpiness)
- Implements save/load for shader configuration
- Selects appropriate shader version based on hardware capabilities
- Manages shader initialization and shutdown

## Key Types
- ShdBumpDiffDefClass (Class): Main shader definition class
- (anonymous enum) (Enum): Chunk IDs for save/load
- CHUNKID_VARIABLES (Enum): Container chunk ID
- VARID_TEXTURE_NAME (Enum): Texture name variable ID
- VARID_BUMP_MAP_NAME (Enum): Bump map name variable ID
- VARID_AMBIENT_COLOR (Enum): Ambient color variable ID
- VARID_DIFFUSE_COLOR (Enum): Diffuse color variable ID
- VARID_DIFFUSE_BUMPINESS (Enum): Bumpiness variable ID

## Key Functions
### ShdBumpDiffDefClass::Save
- Purpose: Serializes shader parameters to a chunk save stream
- Calls: ShdDefClass::Save, _splitpath, strcat, WRITE_MICRO_CHUNK_WWSTRING, WRITE_MICRO_CHUNK

### ShdBumpDiffDefClass::Load
- Purpose: Deserializes shader parameters from a chunk load stream
- Calls: ShdDefClass::Load, Open_Chunk, Open_Micro_Chunk, READ_MICRO_CHUNK_WWSTRING, READ_MICRO_CHUNK

### ShdBumpDiffDefClass::Init
- Purpose: Initializes the appropriate shader version based on hardware capabilities
- Calls: DX8Wrapper::Get_Current_Caps, Shd8BumpDiffClass::Init, Shd7BumpDiffClass::Init, Shd6BumpDiffClass::Init

### ShdBumpDiffDefClass::Shutdown
- Purpose: Shuts down the current shader version
- Calls: Shd8BumpDiffClass::Shutdown, Shd7BumpDiffClass::Shutdown, Shd6BumpDiffClass::Shutdown

### ShdBumpDiffDefClass::Create
- Purpose: Creates an instance of the appropriate shader interface
- Calls: new Shd8BumpDiffClass, new Shd7BumpDiffClass, new Shd6BumpDiffClass

## Globals
- ShdVersion ShdBumpDiffDefClass::Version (Static): Tracks the selected shader version

## Dependencies
- dx8fvf.h, dx8wrapper.h, assetmgr.h, shdbumpd
