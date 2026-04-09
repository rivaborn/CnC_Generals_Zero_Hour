# Generals/Code/Tools/WW3D/max2w3d/boneicon.cpp

## Purpose
Defines the vertex and face data for a bone icon model used in the W3D exporter tool.

## Responsibilities
- Stores vertex coordinates for the bone icon mesh
- Stores face indices for the bone icon mesh
- Provides constants for vertex and face counts
- Suppresses specific compiler warnings for this file

## Key Types
- VertexStruct (struct): 3D vertex coordinates (x, y, z)
- FaceStruct (struct): Triangle face defined by three vertex indices

## Key Functions
None.

## Globals
- NumBoneIconVerts (const int): Number of vertices in the bone icon (184)
- NumBoneIconFaces (const int): Number of faces in the bone icon (366)
- BoneIconVerts (VertexStruct[184]): Array of vertex coordinates for the bone icon mesh
- BoneIconFaces (FaceStruct[366]): Array of face indices for the bone icon mesh

## Dependencies
- "boneicon.h" (header file)
- VertexStruct and FaceStruct definitions (from boneicon.h)
