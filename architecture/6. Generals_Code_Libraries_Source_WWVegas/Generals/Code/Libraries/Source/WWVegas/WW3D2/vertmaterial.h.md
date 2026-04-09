# Generals/Code/Libraries/Source/WWVegas/WW3D2/vertmaterial.h

## Purpose
Defines the VertexMaterialClass, a thin wrapper around Direct3D material properties for the W3D engine.

## Responsibilities
- Manages vertex material properties (colors, shininess, opacity, lighting)
- Handles texture mapping and UV source configuration
- Supports loading/saving materials to W3D files
- Provides material presets and CRC computation for uniqueness

## Key Types
- **VertexMaterialClass (Class)**: Wraps Direct3D material properties for vertex rendering.
- **MappingType (Enum)**: Defines texture mapping types (none, UV, environment).
- **FlagsType (Enum)**: Material flags (depth cue, alpha, specular copy).
- **ColorSourceType (Enum)**: Color source options (material, vertex color arrays).
- **PresetType (Enum)**: Predefined material presets (prelit diffuse/nodiffuse).

## Key Functions
### `Apply()`
- Purpose: Applies material render states to Direct3D.
- Calls: Direct3D API calls (not visible in header).

### `Load_W3D()`
- Purpose: Loads material from W3D file chunk.
- Calls: `ChunkLoadClass` methods.

### `Save_W3D()`
- Purpose: Saves material to W3D file chunk.
- Calls: `ChunkSaveClass` methods.

### `Compute_CRC()`
- Purpose: Computes CRC for material uniqueness.
- Calls: None (internal computation).

## Globals
- **Presets[PRESET_COUNT] (VertexMaterialClass*)**: Static array of material presets.

## Dependencies
- `refcount.h`, `vector3.h`, `w3d_file.h`, `meshbuild.h`, `w3derr.h`, `mapper.h`, `wwstring.h`
- `ChunkLoadClass`, `ChunkSaveClass`, `TextureMapperClass`, `MeshBuilderClass`
