# Generals/Code/Tools/WW3D/max2w3d/SnapPoints.cpp

## Purpose
Handles exporting snap points from 3D Studio Max to W3D format for the game engine.

## Responsibilities
- Filters nodes to find point helpers in the scene
- Collects and exports point positions as W3D vectors
- Writes point data to a chunk in the output file

## Key Types
- **PointFilterClass (Class)**: Filters scene nodes to find point helpers
- **SnapPointsClass (Class)**: Manages point export functionality (defined elsewhere)

## Key Functions
### PointFilterClass::Accept_Node
- Purpose: Determines if a node should be included in the point list
- Calls: `node->EvalWorldState`, `node->IsHidden`, `obj->ClassID`

### SnapPointsClass::Export_Points
- Purpose: Exports all point helper positions to the W3D file
- Calls: `PointFilterClass` constructor, `INodeListClass` constructor, `csave.Begin_Chunk`, `csave.Write`, `csave.End_Chunk`, `node->GetNodeTM`

## Globals
- None

## Dependencies
- `SnapPoints.h`, `chunkio.h`, `Max.h`, `nodelist.h`, `w3d_file.h`
- `INode`, `Object`, `Point3`, `TimeValue`, `W3dVectorStruct`, `ChunkSaveClass`, `INodeFilterClass`, `INodeListClass`
