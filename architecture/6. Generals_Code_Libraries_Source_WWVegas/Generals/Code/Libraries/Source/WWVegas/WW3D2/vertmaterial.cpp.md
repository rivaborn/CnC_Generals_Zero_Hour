# Generals/Code/Libraries/Source/WWVegas/WW3D2/vertmaterial.cpp

## Purpose
Manages vertex material properties and rendering states for the W3D rendering engine.

## Responsibilities
- Handles material properties (colors, shininess, opacity)
- Manages texture mappers for multiple rendering stages
- Provides preset materials and material cloning
- Computes material CRC for change detection
- Applies material states to Direct3D via DX8Wrapper

## Key Types
- **VertexMaterialClass (Class)**: Main material class managing D3D material properties and texture mappers
- **DynD3DMATERIAL8 (Class)**: Dynamic memory pool wrapper for D3DMATERIAL8 (conditional compilation)
- **ColorSourceType (Enum)**: Defines color source types (MATERIAL, COLOR1, COLOR2)

## Key Functions
### VertexMaterialClass::Apply
- Purpose: Applies material properties and texture mappers to Direct3D render states
- Calls: DX8Wrapper::Set_DX8_Material, DX8Wrapper::Set_DX8_Render_State, Mapper[i]->Apply

### VertexMaterialClass::Compute_CRC
- Purpose: Computes a CRC hash of material properties for change detection
- Calls: CRC_Memory

### VertexMaterialClass::Load_W3D
- Purpose: Loads material from W3D format chunk data
- Calls: ChunkLoadClass methods, various NEW_REF texture mapper constructors

### VertexMaterialClass::Init/Shutdown
- Purpose: Initializes/shuts down material presets
- Calls: NEW_REF, REF_PTR_RELEASE

## Globals
- **unique (unsigned int)**: Counter for generating unique material IDs
- **VertexMaterialClass::Presets[VertexMaterialClass::PRESET_COUNT]**: Array of preset materials

## Dependencies
- Direct3D 8 types (D3DMATERIAL8, D3D* constants)
- WW3D engine components (W3DMPO, MeshBuilderClass)
- Utility classes (W3dUtilityClass, DX8Wrapper)
- Memory management (W3DNEW, REF_PTR_RELEASE)
- Chunk I/O system (ChunkLoadClass, ChunkSaveClass)
- INI parsing (IniFileClass, XStrawClass)
