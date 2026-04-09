# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/projector.h

## Purpose
Defines the `ProjectorClass`, a base class for projection handling in the 3D engine, used for texture projection and decals.

## Responsibilities
- Encapsulates projection data (transform and projection matrices).
- Manages bounding volumes for projection.
- Provides texture coordinate computation.
- Supports perspective and orthographic projections.

## Key Types
- **ProjectorClass (Class)**: Base class for projection handling.
- **MatrixMapperClass (Class)**: Used for texture mapping (forward declaration).

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

### Get_Transform() const
- Purpose: Retrieves the transformation matrix.
- Calls: Not inferable.

### Set_Perspective_Projection(float hfov, float vfov, float znear, float zfar)
- Purpose: Configures perspective projection parameters.
- Calls: Not inferable.

### Set_Ortho_Projection(float xmin, float xmax, float ymin, float ymax, float znear, float zfar)
- Purpose: Configures orthographic projection parameters.
- Calls: Not inferable.

### Get_Bounding_Volume() const
- Purpose: Returns the world-space bounding volume.
- Calls: Not inferable.

### Compute_Texture_Coordinate(const Vector3 & point, Vector3 * set_stq)
- Purpose: Computes texture coordinates for a given point.
- Calls: Not inferable.

### Peek_Mapper() const
- Purpose: Returns the matrix mapper.
-
