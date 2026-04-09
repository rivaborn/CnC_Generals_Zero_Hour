# Generals/Code/Libraries/Source/WWVegas/WWLib/binheap.h

## Purpose
Implements a binary heap data structure for managing ordered elements with priority-based operations.

## Responsibilities
- Provides heap operations (insert, remove min, percolate up)
- Manages dynamic resizing of the underlying array
- Supports custom key-based comparison via template
- Tracks element positions within the heap

## Key Types
- **HeapNodeClass (Class)**: Abstract base for heap elements; defines heap location and key access
- **BinaryHeapClass (Class)**: Main heap implementation; manages node ordering and storage

## Key Functions
### BinaryHeapClass::Insert
- Purpose: Adds a node to the heap and maintains order
- Calls: `Greater_Than`, `Set_Heap_Location`

### BinaryHeapClass::Remove_Min
- Purpose: Removes and returns the smallest element, reordering the heap
- Calls: `Less_Than`, `Set_Heap_Location`

### BinaryHeapClass::Percolate_Up
- Purpose: Repositions a node upward if its key decreased
- Calls: `Greater_Than`, `Set_Heap_Location`

### BinaryHeapClass::Resize_Array
- Purpose: Reallocates the internal storage array
- Calls: `Release_Array`, `memset`

## Globals
None

## Dependencies
- `<assert.h>` for debugging checks
- `bittype.h` for uint32 definition
- `W3DNEWARRAY` macro for memory allocation
- `memset` for array initialization
