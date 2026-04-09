# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/projector.cpp

## Purpose
Implements the `ProjectorClass` for handling perspective and orthographic projections in the 3D engine.

## Responsibilities
- Manages projector transformations and projections
- Computes texture coordinates for world-space points
- Updates world-space bounding volumes
- Handles perspective and orthographic projection setups

## Key Types
- `ProjectorClass` (Class): Manages projector transformations and projections
- `Matrix3D` (Type): 3D transformation matrix
- `Vector3` (Type): 3D vector
- `OBBoxClass` (Class): Oriented bounding box

## Key Functions
### `Set_Transform`
- Purpose: Sets the transform for the projector
- Calls: `Update_WS_Bounding_Volume`

### `Set_Perspective_Projection`
- Purpose: Sets up a perspective projection
- Calls: `Mapper->Set_Type`, `Projection.Init_Perspective`, `Update_WS_Bounding_Volume`

### `Set_Ortho_Projection`
- Purpose: Sets up an orthographic projection
- Calls: `Mapper->Set_Type`, `Projection.Init_Ortho`, `Update_WS_Bounding_Volume`

### `Compute_Texture_Coordinate`
- Purpose: Computes texture coordinates for a given world-space point
- Calls: `Mapper->Compute_Texture_Coordinate`

### `Update_WS_Bounding_Volume`
- Purpose: Recalculates the world-space bounding box
- Calls: `OBBoxClass::Transform`

## Globals
- None

## Dependencies
- `projector.h`
- `refcount.h`
- `matrixmapper.h`
- `MatrixMapperClass`
- `Matrix3x3`
- `OBBoxClass`
