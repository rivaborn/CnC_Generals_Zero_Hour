# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DPoly.cpp

## Purpose
Implements polygon clipping functionality for the W3D rendering engine.

## Responsibilities
- Manages polygon vertex storage
- Performs polygon clipping against planes
- Handles vertex addition and removal

## Key Types
- `ClipPolyClass`: Manages polygon vertices and clipping operations

## Key Functions
### `Reset`
- Purpose: Clears all vertices from the polygon
- Calls: `Verts.Delete_All`

### `Add_Vertex`
- Purpose: Adds a new vertex to the polygon
- Calls: `Verts.Add`

### `Clip`
- Purpose: Clips polygon against a plane and stores result in destination polygon
- Calls: `plane.In_Front`, `plane.Compute_Intersection`, `Vector3::Lerp`

## Globals
- None

## Dependencies
- `W3DPoly.h`
- `Lib/BaseType.h`
- `Vector3`
- `PlaneClass`
