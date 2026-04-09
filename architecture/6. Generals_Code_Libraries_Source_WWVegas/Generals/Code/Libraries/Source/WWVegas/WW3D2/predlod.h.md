# Generals/Code/Libraries/Source/WWVegas/WW3D2/predlod.h

## Purpose
Declares the `PredictiveLODOptimizerClass` for managing Level-of-Detail (LOD) optimization in the 3D renderer.

## Responsibilities
- Manages predictive LOD optimization for render objects
- Tracks object costs and visibility
- Optimizes LODs based on a maximum cost threshold
- Allocates/frees memory for object arrays

## Key Types
- **LODHeapNode (Class)**: Not inferable (forward declaration only)
- **PredictiveLODOptimizerClass (Class)**: Core class for predictive LOD optimization

## Key Functions
### `Clear`
- Purpose: Clears the optimizer state
- Calls: Not inferable

### `Add_Object`
- Purpose: Adds a render object to the optimization pool
- Calls: Not inferable

### `Add_Cost`
- Purpose: Accumulates cost for LOD optimization
- Calls: Not inferable

### `Optimize_LODs`
- Purpose: Optimizes LODs based on a maximum cost threshold
- Calls: Not inferable

### `Free`
- Purpose: Frees all allocated memory
- Calls: Not inferable

### `AllocVisibleObjArrays`
- Purpose: Allocates arrays for visible objects
- Calls: Not inferable

## Globals
- **ObjectArray (RenderObjClass\*\*)**: Array of render objects
- **ArraySize (int)**: Size of the object array
- **NumObjects (int)**: Number of objects in the array
- **TotalCost (float)**: Accumulated cost for LOD optimization
- **VisibleObjArray1 (LODHeapNode\*)**: First visible object array
- **VisibleObjArray2 (LODHeapNode\*)**: Second visible
