# Generals/Code/Libraries/Source/WWVegas/WW3D2/predlod.cpp

## Purpose
Implements a predictive LOD (Level of Detail) optimizer for rendering objects, balancing visual quality and performance.

## Responsibilities
- Manages a heap-based priority queue for LOD optimization
- Tracks object costs and values for adaptive rendering
- Implements up/down heap operations for priority queue maintenance
- Handles object reference counting for memory management

## Key Types
- **LODHeapNode (Class)**: Represents a node in the heap with an item and a key for sorting
- **LODHeap (Class)**: Implements a binary heap for priority queue operations
- **PredictiveLODOptimizerClass (External)**: Manages the LOD optimization process (defined elsewhere)

## Key Functions
### LODHeap::Upheap
- Purpose: Moves a node up the heap to maintain heap order
- Calls: None (internal operations only)

### LODHeap::Downheap
- Purpose: Moves a node down the heap to maintain heap order
- Calls: None (internal operations only)

### PredictiveLODOptimizerClass::Optimize_LODs
- Purpose: Adjusts LOD levels to stay within a cost budget
- Calls: LODHeap constructor, Change_Key_Top, Change_Key, Increment_LOD, Decrement_LOD

## Globals
- **ObjectArray (RenderObjClass**)**: Array of objects being optimized
- **VisibleObjArray1/2 (LODHeapNode**)**: Temporary arrays for heap operations
- **NumObjects (int)**: Current count of objects
- **TotalCost (float)**: Sum of all object costs
- **ArraySize (int)**: Capacity of ObjectArray
- **NumVisibleObjects (int)**: Size of visible object arrays

## Dependencies
- `predlod.h` (header)
- `RenderObjClass` (external rendering object class)
- `W3DNEWARRAY` (memory allocation macro)
- `WWASSERT` (assertion macro)
