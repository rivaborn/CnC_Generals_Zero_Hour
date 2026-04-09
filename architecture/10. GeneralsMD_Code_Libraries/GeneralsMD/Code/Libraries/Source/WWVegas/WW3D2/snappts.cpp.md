# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/snappts.cpp

## Purpose
Handles loading of snapshot points data from W3D files for the game engine.

## Responsibilities
- Loads W3D snapshot point data from chunked files
- Converts W3dVectorStruct to Vector3 format
- Manages error handling during file loading
- Resizes internal storage for point data

## Key Types
- SnapPointsClass (Class): Manages collection of snapshot points
- W3dVectorStruct (Struct): Raw vector data from W3D files
- Vector3 (Class): Engine's 3D vector representation

## Key Functions
### SnapPointsClass::Load_W3D
- Purpose: Loads snapshot points from a W3D chunk
- Calls: cload.Cur_Chunk_Length(), cload.Read(), Resize(), Add()

## Globals
None

## Dependencies
- snappts.h (header for SnapPointsClass)
- chunkio.h (chunk loading utilities)
- w3d_file.h (W3D file format definitions)
- w3derr.h (error type definitions)
