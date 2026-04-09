# Generals/Code/Libraries/Source/WWVegas/WWMath/cullsys.cpp

## Purpose
Implements the culling system for spatial partitioning and object collection in the game engine.

## Responsibilities
- Manages cullable objects and their spatial bounds
- Maintains a collection list for iterating through objects
- Provides methods for updating and querying culling state
- Handles object linkage to the culling system

## Key Types
- CullableClass (Class): Base class for objects that can be culled, containing a culling box and linkage
- CullSystemClass (Class): Base class for culling systems that manage collections of cullable objects
- AABoxClass (Not defined here): Used for defining culling volumes

## Key Functions
### CullableClass::Set_Cull_Box
- Purpose: Updates the culling box for an object and notifies the culling system
- Calls: CullSystemClass::Update_Culling

### CullSystemClass::Add_To_Collection
- Purpose: Adds an object to the current collection list
- Calls: None

### CullSystemClass::Reset_Collection
- Purpose: Clears the current collection list
- Calls: None

## Globals
- None

## Dependencies
- cullsys.h: Header for culling system classes
- wwdebug.h: Debug assertion macros
- wwprofile.h: Profiling macros
- Vector3: Used for defining box extents
- WWASSERT: Debug assertion macro
