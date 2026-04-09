# Generals/Code/Tools/WW3D/max2w3d/boneicon.h

## Purpose
Defines data structures and global arrays for bone icon geometry used in 3D model conversion.

## Responsibilities
- Declares vertex and face structures for bone icon representation
- Provides global arrays for bone icon vertices and faces
- Exposes constants for vertex and face counts

## Key Types
- VertexStruct (struct): Stores 3D vertex coordinates (X, Y, Z)
- FaceStruct (struct): Stores indices for three vertices forming a face (V0, V1, V2)

## Key Functions
None

## Globals
- NumBoneIconVerts (int): Number of vertices in the bone icon
- NumBoneIconFaces (int): Number of faces in the bone icon
- BoneIconVerts (VertexStruct[]): Array of vertex data for the bone icon
- BoneIconFaces (FaceStruct[]): Array of face data for the bone icon

## Dependencies
- None (header-only file)
