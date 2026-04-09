# Generals/Code/Tools/WW3D/pluglib/w3d_file.h

## Purpose
Defines data structures and chunk types for W3D file format used in the game's 3D asset pipeline.

## Responsibilities
- Declares chunk ID enums for mesh, hierarchy, animation, and other 3D asset types
- Defines structs for vertices, materials, triangles, and other 3D primitives
- Specifies versioning and header structures for different W3D file components
- Documents the file format's evolution and chunk organization

## Key Types
- W3dChunkHeader (Struct): Chunk identifier and size header
- W3dVectorStruct (Struct): 3D vector with X/Y/Z components
- W3dMaterialStruct (Struct): Version 1 material definition
- W3dMeshHeaderStruct (Struct): Original mesh header with counts and bounds
- W3dMeshHeader3Struct (Struct): Version 3 mesh header with simplified structure

## Key Functions
None - this is a header-only file with no function declarations.

## Globals
None

## Dependencies
- "always.h" - likely contains basic type definitions
- "bittype.h" - for bit manipulation types
- Uses uint32, uint16, uint8, float32 types (likely from always.h)
