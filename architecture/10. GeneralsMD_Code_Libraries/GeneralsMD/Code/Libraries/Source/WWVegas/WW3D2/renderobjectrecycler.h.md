# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/renderobjectrecycler.h

## Purpose
Manages a pool of reusable render objects to optimize memory allocation in the SAGE engine.

## Responsibilities
- Recycles render objects to avoid frequent allocations/deallocations
- Provides methods to acquire and release render objects
- Maintains a list of inactive models for reuse

## Key Types
- RenderObjClass (Class): Base class for render objects
- Matrix3D (Class): 3D transformation matrix
- RenderObjectRecyclerClass (Class): Manages render object recycling

## Key Functions
### Reset
- Purpose: Clears all cached render objects
- Calls: None

### Get_Render_Object
- Purpose: Retrieves a render object from cache or creates a new one
- Calls: None (implementation in .cpp)

### Return_Render_Object
- Purpose: Returns a render object to the cache for reuse
- Calls: Insert_Inactive_Model

### Insert_Inactive_Model
- Purpose: Adds a model to the inactive pool
- Calls: None

### Reset_Model
- Purpose: Resets a model's state before reuse
- Calls: None

## Globals
- InactiveModels (RefRenderObjListClass): Stores available render objects

## Dependencies
- "always.h", "robjlist.h"
- RenderObjClass, Matrix3D (forward declarations)
- RefRenderObjListClass (external)
