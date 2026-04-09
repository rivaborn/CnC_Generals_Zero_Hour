# Generals/Code/Libraries/Source/WWVegas/WW3D2/projector.cpp

## Purpose
Implements the ProjectorClass for handling perspective and orthographic projections in 3D space.

## Responsibilities
- Manages projector transformations and projections
- Computes texture coordinates for world-space points
- Updates world-space bounding volumes
- Handles perspective and orthographic projection setups

## Key Types
- ProjectorClass (Class): Manages projector transformations and projections
- Matrix3D (Type): 3D transformation matrix
- OBBoxClass (Class): Oriented bounding box for spatial queries
- Vector3 (Struct): 3D vector representation
- MatrixMapperClass (Class): Handles texture coordinate computation

## Key Functions
### ProjectorClass::Set_Transform
- Purpose: Sets the transformation matrix for the projector
- Calls: Update_WS_Bounding_Volume

### ProjectorClass::Set_Perspective_Projection
- Purpose: Configures a perspective projection with given FOV and clipping planes
- Calls: Mapper->Set_Type, Projection.Init_Perspective, Update_WS_Bounding_Volume

### ProjectorClass::Set_Ortho_Projection
- Purpose: Configures an orthographic projection with given bounds and clipping planes
- Calls: Mapper->Set_Type, Projection.Init_Ortho, Update_WS_Bounding_Volume

### ProjectorClass::Compute_Texture_Coordinate
- Purpose: Computes texture coordinates for a given world-space point
- Calls: Mapper->Compute_Texture_Coordinate

### ProjectorClass::Update_WS_Bounding_Volume
- Purpose: Recalculates the world-space bounding volume based on current transform
- Calls: OBBoxClass::Transform

## Globals
None

## Dependencies
- projector.h
- refcount.h
- matrixmapper.h
- Matrix3D, OBBoxClass, Vector3, MatrixMapperClass (external types)
