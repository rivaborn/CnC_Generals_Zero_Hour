# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/predlod.h

## Purpose
Declares the `PredictiveLODOptimizerClass` for managing Level-of-Detail (LOD) optimization in the SAGE engine.

## Responsibilities
- Manages predictive LOD optimization for render objects
- Tracks object costs and visibility
- Optimizes LODs based on a maximum cost threshold
- Allocates/frees memory for object arrays

## Key Types
- **LODHeapNode (Class)**: Not inferable (forward declaration only)
- **PredictiveLODOptimizerClass (Class)**: Manages predictive LOD optimization

## Key Functions
### `Clear`
- Purpose: Resets the optimizer state
- Calls: Not inferable

### `Add_Object`
- Purpose: Adds a render object to the optimization pool
- Calls: Not inferable

### `Add_Cost`
- Purpose: Increments the total cost counter
- Calls: Not inferable

### `Optimize_LODs`
- Purpose: Optimizes LODs based on a maximum cost threshold
- Calls: Not inferable

### `Get_Total_Cost`
- Purpose: Returns the total cost of all objects
- Calls: Not inferable

### `Free`
- Purpose: Frees all allocated memory
- Calls: Not inferable

### `AllocVisibleObjArrays`
- Purpose: Allocates memory for visible object arrays
- Calls: Not inferable

## Globals
- **ObjectArray (RenderObjClass\*\*)**: Array of render objects
- **ArraySize (int)**: Size of the object array
- **NumObjects (int)**: Number of objects in the array
- **TotalCost (float)**: Accumulated cost of all objects
- **VisibleObjArray1 (LODHeapNode
