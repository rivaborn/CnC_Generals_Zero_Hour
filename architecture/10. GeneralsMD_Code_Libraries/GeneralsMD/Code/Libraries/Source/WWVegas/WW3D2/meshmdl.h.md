# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshmdl.h

## Purpose
Header file defining the `MeshModelClass` and related classes for 3D mesh rendering in the SAGE engine.

## Responsibilities
- Declares mesh model and rendering-related classes
- Defines interfaces for mesh geometry, materials, and textures
- Provides loading/saving functionality for W3D format
- Manages gap filling for N-patched meshes

## Key Types
- **MeshModelClass (Class)**: Main mesh model container with geometry and material data
- **GapFillerClass (Class)**: Generates gap-filling polygons for N-patched meshes
- **VertexFormatXYZNDUV2 (Struct)**: Vertex format definition
- **TextureClass (Class)**: Texture reference
- **MaterialInfoClass (Class)**: Material information container
- **MeshMatDescClass (Class)**: Material description interface

## Key Functions
### MeshModelClass::Load_W3D
- Purpose: Loads W3D mesh format from chunk loader
- Calls: read_chunks, read_texcoords, read_materials, etc.

### MeshModelClass::Register_For_Rendering
- Purpose: Registers mesh for rendering system
- Calls: Not inferable

### GapFillerClass::Add_Polygon
- Purpose: Adds a polygon to the gap filler
- Calls: Not inferable

## Globals
- None

## Dependencies
- Key includes: vector2.h, vector3.h, vector4.h, sharebuf.h, shader.h, vertmaterial.h
- External symbols: W3DMPO, WW3DErrorType, ChunkLoadClass, MeshLoadContextClass
