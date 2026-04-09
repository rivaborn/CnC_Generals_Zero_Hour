# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/collect.h

## Purpose
Defines the `CollectionClass` render object and its loader, which manages a hierarchy of sub-objects and provides rendering, collision, and transformation capabilities.

## Responsibilities
- Manages a collection of render objects as sub-objects.
- Handles rendering, collision detection, and bounding volume calculations.
- Supports snap points for object attachment.
- Provides proxy interface for special rendering effects.
- Loads collection data from W3D files.

## Key Types
- **CollectionDefClass (Class)**: Not inferable (forward declaration).
- **SnapPointsClass (Class)**: Not inferable (forward declaration).
- **CollectionClass (Class)**: A composite render object containing sub-objects.
- **CollectionLoaderClass (Class)**: Loader for collection objects from W3D files.

## Key Functions
### `CollectionClass::Render`
- Purpose: Renders the collection and its sub-objects.
- Calls: Not inferable (implementation in .cpp).

### `CollectionClass::Cast_Ray`
- Purpose: Performs ray collision testing against the collection.
- Calls: Not inferable.

### `CollectionClass::Get_Obj_Space_Bounding_Sphere`
- Purpose: Retrieves the object-space bounding sphere.
- Calls: Not inferable.

### `CollectionClass::Update_Obj_Space_Bounding_Volumes`
- Purpose: Updates the bounding volumes of the collection.
- Calls: Not inferable.

## Globals
- `_CollectionLoader (CollectionLoaderClass)`: Global instance for loading collections.

## Dependencies
- `rendobj.h`, `composite.h`, `vector.h`, `proto.h`, `w3d_file.h`, `wwstring.h`, `proxy.h`
- `RenderInfoClass`, `SpecialRenderInfoClass`, `RayCollisionTestClass`, `AABox
