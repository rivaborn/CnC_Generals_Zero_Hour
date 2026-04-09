# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3d_dep.cpp

## Purpose
This file implements dependency scanning for W3D (Westwood 3D) model files, identifying external files referenced by meshes, animations, and other W3D objects.

## Responsibilities
- Parses W3D file chunks to extract dependency information
- Handles various W3D object types (meshes, animations, emitters, etc.)
- Converts W3D object names to filenames
- Collects and deduplicates dependency lists

## Key Types
- STLSpecialAlloc (Class): Custom memory allocator wrapper for STL compatibility
- W3dMeshHeader3Struct: Mesh header structure (external)
- W3dAnimHeaderStruct: Animation header structure (external)
- W3dCompressedAnimHeaderStruct: Compressed animation header (external)
- W3dHModelHeaderStruct: Hierarchical model header (external)
- W3dEmitterInfoStruct: Emitter information (external)
- W3dAggregateInfoStruct: Aggregate object information (external)
- W3dAggregateSubobjectStruct: Aggregate subobject information (external)
- W3dHLodHeaderStruct: Hierarchical LOD header (external)

## Key Functions
### Get_W3D_Dependencies
- Purpose: Main entry point that scans a W3D file and returns its dependencies
- Calls: Get_W3D_Name, Scan_Chunk, file I/O operations

### Scan_Chunk
- Purpose: Dispatches chunk scanning based on chunk type
- Calls: Scan_Mesh, Scan_Anim, Scan_Compressed_Anim, Scan_HModel, Scan_Emitter, Scan_Aggregate, Scan_HLOD

### Scan_Mesh
- Purpose: Scans mesh chunks for dependencies
- Calls: Scan_Mesh_Header, Scan_Mesh_Textures

### Scan_Mesh_Textures
- Purpose: Extracts texture filenames from mesh texture chunks
- Calls: None (direct file reading)

### Get_W3D_Name
- Purpose: Extracts object name from W3D filename
- Calls: strrchr, strlen, strncpy, strupr

### Make_W3D_Filename
- Purpose: Converts W3D object name to filename with .w3d extension
- Calls: strchr, strlwr, strcat

## Globals
- None

## Dependencies
- w3d_dep.h: Header for this module
- w3d_file.h: W3D file I/O
- chunkio.h: Chunk I/O utilities
- ffactory.h: File factory interface
- STL containers (StringList)
- C runtime functions (strrchr, strlen, etc.)
