# Generals/Code/Libraries/Source/WWVegas/WW3D2/collect.h

## Purpose
Defines the `CollectionClass` render object and its loader, which manages a hierarchy of sub-objects and provides collision, rendering, and transformation capabilities.

## Responsibilities
- Manages a collection of render objects as sub-objects
- Handles rendering, collision detection, and bounding volumes
- Provides snap point management and transformation operations
- Loads collection data from W3D files via `CollectionLoaderClass`

## Key Types
- **CollectionDefClass (Class)**: Not inferable (forward declaration).
- **SnapPointsClass (Class)**: Not inferable (forward declaration).
- **CollectionClass (Class)**: A composite render object containing sub-objects with rendering, collision, and transformation support.
- **CollectionLoaderClass (Class)**: Prototype loader for W3D collection chunks.

## Key Functions
### `CollectionClass::Render`
- Purpose: Renders the collection and its sub-objects.
- Calls: Not inferable from header.

### `CollectionClass::Cast_Ray`
- Purpose: Performs ray collision testing against the collection.
- Calls: Not inferable from header.

### `CollectionClass::Get_Obj_Space_Bounding_Sphere`
- Purpose: Retrieves the object-space bounding sphere.
- Calls: Not inferable from header.

### `CollectionLoaderClass::Load_W3D`
- Purpose: Loads a collection prototype from a W3D chunk.
- Calls: Not inferable from header.

## Globals
- `_CollectionLoader (CollectionLoaderClass)`: Global instance of the collection loader.

## Dependencies
- `rendobj.h`, `composite.h`, `vector.h`, `proto.h`, `w3d_file.h`, `wwstring.h`, `proxy.h`
- `RenderInfoClass`, `SpecialRenderInfoClass`, `RayCollisionTest
