# Generals/Code/Libraries/Source/WWVegas/WWMath/cullsys.h

## Purpose
Defines the core culling system architecture for spatial partitioning and object visibility management in the SAGE engine.

## Responsibilities
- Declares base classes for cullable objects and culling systems
- Provides linkage mechanisms between objects and culling systems
- Defines interfaces for object collection and visibility testing
- Manages axis-aligned bounding boxes for spatial queries

## Key Types
- **CullLinkClass (Class)**: Base class for culling system linkage data
- **CullableClass (Class)**: Base class for objects that can be culled (uses ref-counting)
- **CullSystemClass (Class)**: Base class for culling systems (manages object collections)
- **FrustumClass (Class)**: Forward-declared (used for frustum culling)
- **AABoxClass (Class)**: Used for axis-aligned bounding box representation

## Key Functions
### CullableClass::Set_Cull_Box
- Purpose: Updates the object's bounding box and notifies the culling system
- Calls: Not inferable (implementation in .cpp)

### CullSystemClass::Collect_Objects
- Purpose: Populates the collection list with objects intersecting the given primitive
- Calls: Add_To_Collection

### CullSystemClass::Update_Culling
- Purpose: Notifies the system that an object has moved or changed size
- Calls: Not inferable

### CullSystemClass::Add_To_Collection
- Purpose: Adds an object to the internal collection list
- Calls: Not inferable

## Globals
- None

## Dependencies
- Key includes: "wwdebug.h", "stdlib.h", "refcount.h", "aabox.h"
- External symbols: RefCountClass, AABoxClass, OBBoxClass, Vector3
