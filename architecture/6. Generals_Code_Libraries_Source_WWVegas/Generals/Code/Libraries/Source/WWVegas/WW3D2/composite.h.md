# Generals/Code/Libraries/Source/WWVegas/WW3D2/composite.h

## Purpose
Defines the `CompositeRenderObjClass`, a base class for render objects that contain sub-objects, encapsulating common composite object behaviors.

## Responsibilities
- Manages naming and base model naming for composite objects
- Handles bounding volume updates and queries
- Provides collision testing interfaces (ray, box)
- Supports decal creation/deletion
- Encapsulates sub-object notification logic

## Key Types
- **CompositeRenderObjClass (Class)**: Base class for composite render objects that manage sub-objects.

## Key Functions
### CompositeRenderObjClass()
- Purpose: Default constructor.
- Calls: Not inferable.

### ~CompositeRenderObjClass()
- Purpose: Destructor.
- Calls: Not inferable.

### Restart()
- Purpose: Restarts the composite object.
- Calls: Not inferable.

### Get_Name()
- Purpose: Returns the object's name.
- Calls: Not inferable.

### Set_Name()
- Purpose: Sets the object's name.
- Calls: Not inferable.

### Set_Base_Model_Name()
- Purpose: Sets the base model name.
- Calls: Not inferable.

### Get_Num_Polys()
- Purpose: Returns the number of polygons.
- Calls: Not inferable.

### Notify_Added()
- Purpose: Notifies when the object is added to a scene.
- Calls: Not inferable.

### Notify_Removed()
- Purpose: Notifies when the object is removed from a scene.
- Calls: Not inferable.

### Cast_Ray()
- Purpose: Performs ray collision testing.
- Calls: Not inferable.

### Cast_AABox()
- Purpose: Performs axis-aligned box collision testing.
- Calls: Not inferable.

### Cast_OBBox()
- Purpose:
