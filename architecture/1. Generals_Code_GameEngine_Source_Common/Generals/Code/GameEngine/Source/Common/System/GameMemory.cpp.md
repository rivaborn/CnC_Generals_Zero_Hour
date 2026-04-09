# Generals/Code/GameEngine/Source/Common/System/GameMemory.cpp

## Purpose
This file implements the memory management system for Command & Conquer Generals, including allocation, deallocation, and debugging features.

## Responsibilities
- Manage memory allocation and deallocation.
- Provide debug information about memory usage.
- Handle stack traces for memory allocations in debug mode.
- Override global `new` and `delete` operators.

## Key Types
- **MemoryPoolSingleBlock (Class)**: Manages single blocks of memory within a pool.
- **MemoryPoolBlob (Class)**: Represents a blob of memory that can be divided into smaller blocks.
- **None**: No enums defined in this file.

## Key Functions
### roundUpMemBound
- Purpose: Rounds up a given integer to the nearest multiple of `MEM_BOUND_ALIGNMENT`.
- Calls: None

### sysAllocate
- Purpose: Allocates memory and initializes it to zero.
- Calls: `GlobalAlloc`, `memset32`

### sysAllocateDoNotZero
- Purpose: Allocates memory without initializing it.
- Calls: `GlobalAlloc`, `memset32`

### sysFree
- Purpose: Frees allocated memory.
- Calls: `GlobalFree`, `memset32`

### memset32
- Purpose: Fills memory with a 32-bit value.
- Calls: None

### initMemoryManager
- Purpose: Initializes the memory manager and creates necessary objects.
- Calls: `sysAllocate`, `MemoryPoolFactory::init`, `createDynamicMemoryAllocator`, `userMemoryManagerInitPools`

### isMemoryManagerOfficiallyInited
- Purpose: Checks if the memory manager has been officially initialized.
- Calls: None

### preMainInitMemoryManager
- Purpose: Initializes the memory manager before `main` is called.
- Calls: `sysAllocate`, `MemoryPoolFactory::init`, `createDynamicMemoryAllocator`

### shutdownMemoryManager
- Purpose: Shuts down the memory manager and frees all allocated memory.
- Calls: `destroyDynamicMemoryAllocator`, `~MemoryPoolFactory`, `sysFree`

### createW3DMemPool
- Purpose: Creates a new memory pool for W3D.
- Calls: `preMainInitMemoryManager`, `createMemoryPool`

### allocateFromW3DMemPool
- Purpose: Allocates a block from a specified memory pool.
- Calls: `allocateBlock`

### freeFromW3DMemPool
- Purpose: Frees a block back to its memory pool.
- Calls: `freeBlock`

## Globals
- **thePreMainInitFlag (Bool)**: Indicates if the memory manager was initialized before `main`.
- **theMainInitFlag (Bool)**: Indicates if the memory manager is officially initialized.
- **TheMemoryPoolFactory**: Factory for creating memory pools.
- **TheDynamicMemoryAllocator**: Allocator for dynamic memory.
- **theLinkTester (Int)**: Used to test linking of new/delete operators.

## Dependencies
- Includes: `PreRTS.h`, `GameMemory.h`, `CriticalSection.h`, `Errors.h`, `GlobalData.h`, `PerfTimer.h`
- External symbols: `GlobalAlloc`, `GlobalFree`, `memset32`, `StackDumpFromAddresses`
