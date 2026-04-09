# Generals/Code/Tools/WW3D/max2w3d/SnapPoints.h

## Purpose
Header file defining the SnapPointsClass for exporting helper points in 3D models.

## Responsibilities
- Declares SnapPointsClass with static export functionality
- Defines interface for exporting helper points as chunks
- Provides static method for point export

## Key Types
- ChunkSaveClass (Class): Not inferable.
- INode (Class): Not inferable.
- SnapPointsClass (Class): Handles export of helper points for W3D objects.

## Key Functions
### SnapPointsClass::Export_Points
- Purpose: Exports helper points from a scene to a chunk save object.
- Calls: None visible in header.

## Globals
None

## Dependencies
- "Max.h" (3ds Max SDK header)
- ChunkSaveClass (forward declared)
- INode (forward declared)
