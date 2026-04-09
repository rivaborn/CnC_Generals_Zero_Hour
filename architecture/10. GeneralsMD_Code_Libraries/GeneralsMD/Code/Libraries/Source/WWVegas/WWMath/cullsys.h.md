# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/cullsys.h

## Purpose
Defines the core culling system classes for spatial partitioning and object visibility management in the SAGE engine.

## Responsibilities
- Declares base classes for cullable objects and culling systems
- Provides linkage infrastructure between objects and culling systems
- Defines collection mechanisms for spatial queries
- Manages axis-aligned bounding boxes for culling

## Key Types
- **CullLinkClass (Class)**: Base class for culling system linkage data
- **CullableClass (Class)**: Base class for objects that can be culled (uses ref-counting)
- **CullSystemClass (Class)**: Base class for culling systems that manage spatial queries
- **FrustumClass (Class)**: Forward-declared frustum class for view-frustum culling
- **AABoxClass (Class)**: Used for axis-aligned bounding box representation

## Key Functions
### CullableClass::Set_Cull_Box
- Purpose: Updates the object's bounding box and notifies the culling system
- Calls: Not inferable (implementation in .cpp)

### CullSystemClass::Collect_Objects
- Purpose: Populates the collection list with objects intersecting the given primitive
- Calls: Add_To_Collection

### CullSystemClass::Update_Culling
- Purpose: Updates culling data when an object moves or changes size
- Calls: Not inferable

### CullSystemClass::Add_To_Collection
- Purpose: Adds an object to the current collection list
- Calls: Set_Next_Collected

## Globals
- None

## Dependencies
- Key includes: "wwdebug.h", "stdlib.h", "refcount.h", "aabox.h"
- External symbols: RefCountClass, AABoxClass, OBBoxClass, Vector3
