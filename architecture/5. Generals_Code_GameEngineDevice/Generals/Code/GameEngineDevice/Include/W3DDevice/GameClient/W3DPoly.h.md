# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DPoly.h

## Purpose
Defines a polygon clipping utility class for 3D operations in the W3D engine.

## Responsibilities
- Provides polygon clipping functionality against planes
- Manages dynamic vertex storage for polygons
- Supports polygon reset and vertex addition

## Key Types
- ClipPolyClass (Class): polygon clipping utility with vertex management

## Key Functions
### ClipPolyClass::Reset
- Purpose: Clears the polygon's vertex list
- Calls: None

### ClipPolyClass::Add_Vertex
- Purpose: Adds a vertex to the polygon
- Calls: None

### ClipPolyClass::Clip
- Purpose: Clips the polygon against a plane and stores result in destination
- Calls: None

## Globals
- None

## Dependencies
- `vector3.h` (Vector3)
- `plane.h` (PlaneClass)
- `simplevec.h` (SimpleDynVecClass)
