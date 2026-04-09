# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshdam.cpp

## Purpose
Handles mesh damage data loading and management for the W3D engine, including vertex and color damage states.

## Responsibilities
- Loads damage data from W3D files
- Manages damage vertex and color arrays
- Processes damage chunks (vertices/colors)
- Memory allocation/deallocation for damage data

## Key Types
- **DamageClass (Class)**: Manages mesh damage data (vertices/colors)
- **DamageVertexStruct (Struct)**: Stores vertex damage info
- **DamageColorStruct (Struct)**: Stores color damage info
- **W3dMeshDamageStruct (Struct)**: Damage header data

## Key Functions
### DamageClass::Load
- Purpose: Loads damage data from a W3D file
- Calls: `cload.Open_Chunk()`, `cload.Read()`, `cload.Close_Chunk()`, `read_vertices()`, `read_colors()`

### DamageClass::read_vertices
- Purpose: Reads damage vertex data from W3D file
- Calls: `cload.Read()`, `basemesh->getVertexLoc()`

### DamageClass::read_colors
- Purpose: Reads damage color data from W3D file
- Calls: `cload.Read()`

## Globals
None

## Dependencies
- `meshdam.h`, `w3d_file.h`, `w3derr.h`, `chunkio.h`
- `ChunkLoadClass`, `MeshModelClass`, `WW3DErrorType`
- `srVector3` (external vector type)
