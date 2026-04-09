# GeneralsMD/Code/GameEngine/Include/Common/GameMemory.h

## Purpose
Memory management header defining custom allocators, memory pools, and debugging utilities for the SAGE engine.

## Responsibilities
- Declares memory pool system (MemoryPool, DynamicMemoryAllocator)
- Provides custom new/delete operators
- Defines checkpointing and debugging mechanisms
- Exposes memory management utilities for game objects

## Key Types
- **MemoryPool (Class)**: Manages fixed-size memory blocks
- **DynamicMemoryAllocator (Class)**: Handles variable-sized allocations via sub-pools
- **MemoryPoolFactory (Class)**: Creates and manages pools/allocators
- **MemoryPoolObject (Class)**: Base class for pool-allocated objects
- **PoolInitRec (Struct)**: Configuration for pool creation
- **STLSpecialAlloc (Class)**: STL allocator adapter

## Key Functions
### initMemoryManager
- Purpose: Initializes global memory management system
- Calls: userMemoryManagerGetDmaParms, userMemoryManagerInitPools

### shutdownMemoryManager
- Purpose: Cleans up memory management system
- Calls: None

### operator new/delete
- Purpose: Custom global allocators
- Calls: TheDynamicMemoryAllocator methods

## Globals
- **TheMemoryPoolFactory (MemoryPoolFactory*)**: Global factory instance
- **TheDynamicMemoryAllocator (DynamicMemoryAllocator*)**: Global allocator instance

## Dependencies
- BaseType.h, Debug.h, Errors.h
- <new.h>, <stdio.h>
- MEMORYPOOL_DEBUG, MEMORYPOOL_CHECKPOINTING macros
