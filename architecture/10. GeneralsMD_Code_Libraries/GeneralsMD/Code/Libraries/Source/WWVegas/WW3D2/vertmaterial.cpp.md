# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/vertmaterial.cpp

## Purpose
Manages vertex material properties and rendering states for the W3D rendering engine.

## Responsibilities
- Handles material properties (colors, shininess, opacity)
- Manages texture mappers for multiple rendering stages
- Provides preset materials and material cloning
- Applies material states to Direct3D via DX8Wrapper
- Computes CRC for material comparison

## Key Types
- **VertexMaterialClass (Class)**: Main material class managing D3D material properties and texture mappers
- **DynD3DMATERIAL8 (Class)**: Dynamic memory pool wrapper for D3DMATERIAL8 (conditional compilation)
- **ColorSourceType (Enum)**: Defines color source types (MATERIAL, COLOR1, COLOR2)

## Key Functions
### VertexMaterialClass::Apply
- Purpose: Applies material properties and texture mappers to Direct3D
- Calls: DX8Wrapper::Set_DX8_Material, DX8Wrapper::Set_DX8_Render_State, Mapper[i]->Apply

### VertexMaterialClass::Compute_CRC
- Purpose: Computes a CRC hash of the material's properties for comparison
- Calls: CRC_Memory

### VertexMaterialClass::Init/Shutdown
- Purpose: Initializes/shuts down material presets
- Calls: NEW_REF, REF_PTR_RELEASE

### VertexMaterialClass::operator=
- Purpose: Assignment operator for material copying
- Calls: Mapper[i]->Release_Ref, Set_Mapper, Clone

## Globals
- **unique (unsigned int)**: Counter for generating unique material IDs
- **Presets[PRESET_COUNT] (VertexMaterialClass*)**: Array of material presets

## Dependencies
- **Headers**: vertmaterial.h, realcrc.h, wwdebug.h, w3d_util.h, chunkio.h, w3derr.h, ini.h, xstraw.h, dx8wrapper.h
- **External**: D3DMATERIAL8, DX8Wrapper class, TextureMapperClass hierarchy, MeshBuilderClass constants
