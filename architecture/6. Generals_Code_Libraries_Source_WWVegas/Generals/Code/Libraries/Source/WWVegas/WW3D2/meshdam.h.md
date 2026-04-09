# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshdam.h

## Purpose
Header file defining the `DamageClass` for applying damage effects to 3D meshes in the SAGE engine.

## Responsibilities
- Defines data structures for vertex and color damage states
- Declares `DamageClass` for loading and applying mesh damage
- Provides interface for chunk-based loading of damage data

## Key Types
- `RGBStruct` (struct): RGB color component storage
- `DamageVertexStruct` (struct): Stores original/damaged vertex positions
- `DamageColorStruct` (struct): Stores original/damaged vertex colors
- `DamageClass` (class): Manages mesh damage application

## Key Functions
### `Load_W3D`
- Purpose: Loads damage data from a W3D chunk
- Calls: `read_vertices`, `read_colors`

### `read_vertices`
- Purpose: Reads vertex damage data from chunk
- Calls: Not inferable

### `read_colors`
- Purpose: Reads color damage data from chunk
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `vector3.h`, `bittype.h`, `w3derr.h`
- `MeshModelClass`, `ChunkLoadClass` (forward declarations)
- `WW3DErrorType` (enum from `w3derr.h`)
