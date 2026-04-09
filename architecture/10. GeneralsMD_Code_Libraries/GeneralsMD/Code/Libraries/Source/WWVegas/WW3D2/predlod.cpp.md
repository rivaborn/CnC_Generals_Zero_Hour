# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/predlod.cpp

## Purpose
Implements a predictive LOD (Level of Detail) optimizer for rendering performance.

## Responsibilities
- Manages a heap-based priority queue for LOD optimization
- Tracks object costs and values for adaptive rendering
- Implements the Funkhouser-Sequin algorithm for LOD selection
- Handles memory allocation/deallocation for optimization data structures

## Key Types
- **LODHeapNode (Class)**: Represents a node in the heap with a RenderObjClass pointer and a key value
- **LODHeap (Class)**: Implements a binary heap data structure for priority queue operations
- **PredictiveLODOptimizerClass (External)**: Manages the overall LOD optimization process (defined elsewhere)

## Key Functions
### PredictiveLODOptimizerClass::Optimize_LODs
- Purpose: Adjusts LOD levels to stay within a target cost budget
- Calls: LODHeap constructor, Change_Key_Top, Change_Key, Increment_LOD, Decrement_LOD

### LODHeap::Upheap
- Purpose: Moves a node up the heap to maintain heap order
- Calls: None (direct array operations)

### LODHeap::Downheap
- Purpose: Moves a node down the heap to maintain heap order
- Calls: None (direct array operations)

## Globals
- **ObjectArray (RenderObjClass**)**: Stores pointers to render objects
- **TotalCost (float)**: Tracks cumulative rendering cost
- **VisibleObjArray1/2 (LODHeapNode**)**: Temporary arrays for heap operations
- **ArraySize/NumObjects/VisibleObjArraySize (int)**: Track array dimensions and object counts

## Dependencies
- **predlod.h**: Header for PredictiveLODOptimizerClass
- **RenderObjClass**: External class representing renderable objects
- **W3D memory allocation macros**: W3DNEWARRAY
- **Math constants**: FLT_MAX
