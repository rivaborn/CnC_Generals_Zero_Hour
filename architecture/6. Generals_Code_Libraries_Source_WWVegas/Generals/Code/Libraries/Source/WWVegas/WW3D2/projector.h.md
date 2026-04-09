# Generals/Code/Libraries/Source/WWVegas/WW3D2/projector.h

## Purpose
Defines the `ProjectorClass`, a base class for projection operations in the 3D engine, used by texture projectors and decal generators.

## Responsibilities
- Encapsulates projection transformation data
- Provides methods for setting perspective/orthographic projections
- Manages bounding volumes for projection
- Computes texture coordinates for points

## Key Types
- **ProjectorClass (Class)**: Base class for projection operations.
- **MatrixMapperClass (Class)**: Used internally (forward declared).

## Key Functions
### ProjectorClass()
- Purpose: Constructor.
- Calls: Not inferable.

### ~ProjectorClass()
- Purpose: Destructor.
- Calls: Not inferable.

### Set_Transform(const Matrix3D & tm)
- Purpose: Sets the transformation matrix.
- Calls: Not inferable.

### Get_Transform()
- Purpose: Returns the transformation matrix.
- Calls: Not inferable.

### Set_Perspective_Projection(float hfov, float vfov, float znear, float zfar)
- Purpose: Configures perspective projection parameters.
- Calls: Not inferable.

### Set_Ortho_Projection(float xmin, float xmax, float ymin, float ymax, float znear, float zfar)
- Purpose: Configures orthographic projection parameters.
- Calls: Not inferable.

### Get_Bounding_Volume()
- Purpose: Returns the world-space bounding volume.
- Calls: Not inferable.

### Compute_Texture_Coordinate(const Vector3 & point, Vector3 * set_stq)
- Purpose: Computes texture coordinates for a given point.
- Calls: Not inferable.

### Update_WS_Bounding_Volume()
- Purpose: Updates the world-space bounding volume.
- Calls
