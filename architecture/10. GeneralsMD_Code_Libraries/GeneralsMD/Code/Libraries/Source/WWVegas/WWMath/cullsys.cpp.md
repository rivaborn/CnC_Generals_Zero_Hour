# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/cullsys.cpp

## Purpose
Implements the culling system for spatial partitioning and object collection in the game engine.

## Responsibilities
- Manages cullable objects and their spatial bounds
- Maintains a collection list for iterating through visible objects
- Handles updates to object culling boxes
- Provides methods for traversing collected objects

## Key Types
- CullableClass (Class): Base class for objects that can be culled, containing a culling box and linkage
- CullSystemClass (Class): Base class for culling systems that manage collections of cullable objects

## Key Functions
### CullableClass::Set_Cull_Box
- Purpose: Updates the culling box for an object and notifies the culling system
- Calls: CullSystemClass::Update_Culling

### CullSystemClass::Add_To_Collection
- Purpose: Adds an object to the collection list for iteration
- Calls: None

### CullSystemClass::Reset_Collection
- Purpose: Clears the collection list
- Calls: None

## Globals
- None

## Dependencies
- cullsys.h (header for culling system classes)
- wwdebug.h (assertions and debugging)
- wwprofile.h (profiling macros)
- Vector3 (used in AABoxClass initialization)
- AABoxClass (axis-aligned bounding box)
