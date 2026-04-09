# Generals/Code/Libraries/Source/WWVegas/WW3D2/snappts.cpp

## Purpose
Handles loading of snapshot points data from W3D files for the game engine.

## Responsibilities
- Loads W3D snapshot points data from chunked file format
- Converts W3dVectorStruct data into internal Vector3 format
- Manages error handling during file loading
- Resizes internal storage to match loaded data count

## Key Types
- SnapPointsClass (Class): Manages collection of snapshot points
- W3dVectorStruct (Struct): External W3D vector format
- Vector3 (Class): Internal 3D vector representation

## Key Functions
### SnapPointsClass::Load_W3D
- Purpose: Loads snapshot points from a W3D chunk file
- Calls: cload.Cur_Chunk_Length(), cload.Read(), Resize(), Add()

## Globals
None

## Dependencies
- snappts.h (header for SnapPointsClass)
- chunkio.h (chunk loading utilities)
- w3d_file.h (W3D file format definitions)
- w3derr.h (error type definitions)
