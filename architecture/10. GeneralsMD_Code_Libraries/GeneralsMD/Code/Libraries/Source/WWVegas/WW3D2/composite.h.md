# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/composite.h

## Purpose
Defines the `CompositeRenderObjClass`, a base class for render objects that contain sub-objects, encapsulating common composite object behaviors.

## Responsibilities
- Provides default implementations for composite render object operations
- Manages object naming and model hierarchy
- Handles collision tests and bounding volume updates
- Supports decal management and user data attachment

## Key Types
- **CompositeRenderObjClass (Class)**: Base class for composite render objects that contain sub-objects

## Key Functions
### CompositeRenderObjClass()
- Purpose: Default constructor
- Calls: Not inferable

### ~CompositeRenderObjClass()
- Purpose: Destructor
- Calls: Not inferable

### Restart()
- Purpose: Restarts the composite object
- Calls: Not inferable

### Cast_Ray()
- Purpose: Performs ray collision test against the composite object
- Calls: Not inferable

### Cast_AABox()
- Purpose: Performs axis-aligned box collision test
- Calls: Not inferable

### Cast_OBBox()
- Purpose: Performs oriented bounding box collision test
- Calls: Not inferable

### Intersect_AABox()
- Purpose: Tests intersection with axis-aligned box
- Calls: Not inferable

### Intersect_OBBox()
- Purpose: Tests intersection with oriented bounding box
- Calls: Not inferable

### Create_Decal()
- Purpose: Creates a decal on the composite object
- Calls: Not inferable

### Delete_Decal()
- Purpose: Removes a decal from the composite object
- Calls: Not inferable

### Update_Obj_Space_Bounding_Volumes()
- Purpose: Updates the object-space bounding volumes
- Calls: Not inferable
