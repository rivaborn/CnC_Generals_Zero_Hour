# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/vertmaterial.h

## Purpose
Defines the VertexMaterialClass, a thin wrapper around Direct3D vertex material properties for the W3D engine.

## Responsibilities
- Manages vertex material properties (colors, shininess, opacity, lighting)
- Handles texture mapping and mapper configurations
- Supports W3D file loading/saving
- Provides material presets and CRC computation

## Key Types
- **VertexMaterialClass (Class)**: Wraps Direct3D vertex material properties.
- **MappingType (Enum)**: Defines UV mapping types (none, UV, environment).
- **FlagsType (Enum)**: Material flags (depth cue, depth cue to alpha, copy specular to diffuse).
- **ColorSourceType (Enum)**: Color source types (material, color1, color2).
- **PresetType (Enum)**: Material presets (prelit diffuse, prelit nodiffuse).

## Key Functions
### `Set_Mapper`
- Purpose: Sets the texture mapper for a given stage.
- Calls: `REF_PTR_SET`

### `Get_Mapper`
- Purpose: Retrieves the texture mapper for a given stage.
- Calls: `Add_Ref`

### `Do_Mappers_Need_Normals`
- Purpose: Checks if any mappers require vertex normals.
- Calls: `Needs_Normals`

### `Are_Mappers_Time_Variant`
- Purpose: Checks if any mappers are time-variant.
- Calls: `Is_Time_Variant`

### `Load_W3D`
- Purpose: Loads material data from a W3D file.
- Calls: Not inferable (external to this file).

### `Save_W3D`
- Purpose: Saves material data to a W3D file.
- Calls: Not inferable (external to this file).

## Globals
- **Presets (VertexMaterialClass*)**: Array of material presets.

## Dependencies
- `refcount.h`, `vector3.h`, `w3d_file.h`, `meshbuild.h`, `w3derr.h`, `mapper.h`, `wwstring.h`
- `ChunkLoadClass`, `ChunkSaveClass`, `DynD3DMATERIAL8`, `TextureMapperClass`
