# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshdam.cpp

## Purpose
Handles loading and processing mesh damage data from W3D files for the game's 3D rendering system.

## Responsibilities
- Loads damage vertex and color data from W3D chunks
- Manages DamageClass lifecycle (construction/destruction)
- Processes damage header information
- Allocates/deallocates vertex and color arrays

## Key Types
- DamageClass (Class): Manages mesh damage data (vertices, colors, materials)
- DamageVertexStruct (Struct): Stores original and damaged vertex positions
- DamageColorStruct (Struct): Stores original and damaged vertex colors

## Key Functions
### DamageClass::Load
- Purpose: Loads damage data from a W3D file chunk
- Calls: cload.Open_Chunk(), cload.Read(), cload.Close_Chunk()

### DamageClass::read_vertices
- Purpose: Reads damage vertex data from W3D file
- Calls: cload.Read(), basemesh->getVertexLoc()

### DamageClass::read_colors
- Purpose: Reads damage color data from W3D file
- Calls: cload.Read()

## Globals
None

## Dependencies
- meshdam.h (header)
- w3d_file.h (W3D file I/O)
- w3derr.h (error types)
- chunkio.h (chunk loading)
- sr.hpp (vector math, commented out)
