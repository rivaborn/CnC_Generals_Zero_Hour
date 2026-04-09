# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSaveDefs.h

## Purpose
Defines data structures and chunk IDs for mesh deformation serialization in the 3D asset pipeline.

## Responsibilities
- Declares chunk ID enums for deformation data serialization
- Defines core deformation data structures (chunk headers, keyframes, vertex data)
- Establishes the binary layout for deformation data export from 3DS Max

## Key Types
- DEFORM_CHUNK_IDS (Enum): Chunk type identifiers for deformation data
- DeformChunk (Struct): Header for deformation data containing set count
- DeformChunkSetInfo (Struct): Metadata for a deformation set (keyframes, flags, vertex counts)
- DeformChunkKeyframeInfo (Struct): Keyframe-specific data (deformation percentage, vertex/color counts)
- DeformDataChunk (Struct): Per-vertex deformation data (index, color index, 3D value)

## Key Functions
None

## Globals
None

## Dependencies
- `<Max.h>`: 3DS Max SDK headers
- `Point3`: 3D point structure (external)
