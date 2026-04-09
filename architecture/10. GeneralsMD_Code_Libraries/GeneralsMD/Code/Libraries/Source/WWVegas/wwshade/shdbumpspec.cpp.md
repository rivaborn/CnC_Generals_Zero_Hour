# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpspec.cpp

## Purpose
Defines the `ShdBumpSpecDefClass` shader class for bump mapping and specular effects, handling save/load and shader version selection.

## Responsibilities
- Manages bump map and specular shader parameters (colors, bumpiness).
- Handles serialization (save/load) of shader properties.
- Selects appropriate shader version (6, 7, or 8) based on hardware capabilities.
- Registers the shader class with the shader factory.

## Key Types
- `ShdBumpSpecDefClass` (Class): Bump specular shader definition with texture and color parameters.
- `(anonymous enum)` (Enum): Chunk IDs for serialization.
- `VARID_*` (Enums): Variable IDs for texture names, colors, and bumpiness values.

## Key Functions
### `Save`
- Purpose: Serializes shader properties to a chunk save stream.
- Calls: `ShdDefClass::Save`, `WRITE_MICRO_CHUNK_WWSTRING`, `WRITE_MICRO_CHUNK`.

### `Load`
- Purpose: Deserializes shader properties from a chunk load stream.
- Calls: `ShdDefClass::Load`, `READ_MICRO_CHUNK_WWSTRING`, `READ_MICRO_CHUNK`.

### `Init`
- Purpose: Initializes the appropriate shader version based on hardware capabilities.
- Calls: `DX8Wrapper::Get_Current_Caps`, `Shd6BumpSpecClass::Init`, `Shd7BumpSpecClass::Init`, `Shd8BumpSpecClass::Init`.

### `Create`
- Purpose: Creates a shader interface instance of the selected version.
- Calls: `Shd6BumpSpecClass`, `Shd7BumpSpecClass`, `Shd8BumpSpecClass` constructors.

## Globals
- `Version` (ShdVersion): Static member tracking the selected shader version.

## Dependencies
- `dx8fvf.h`, `dx8wrapper.h`, `assetmgr.h`, `shdbumpspec.h`, `shd6bumpspec.h`, `shd7bumpspec.h`, `shd8bumpspec.h`, `editable.h`, `shdclassids.h`, `shddeffactory.h`, `shdinterface.h`, `persistfactory.h`, `wwhack.h`.
- `DECLARE_FORCE_LINK`, `REGISTER_SHDDEF`, `NAMED_TEXTURE_FILENAME_PARAM`, `NAMED_EDITABLE_PARAM`.
