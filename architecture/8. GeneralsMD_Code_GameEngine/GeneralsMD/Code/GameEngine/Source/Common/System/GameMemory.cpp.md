# GeneralsMD/Code/GameEngine/Source/Common/System/GameMemory.cpp

## Purpose
Memory management system for the game engine, implementing custom allocators, memory pools, and debugging tools.

## Responsibilities
- Implements custom memory allocation/deallocation
- Manages memory pools and dynamic memory allocators
- Provides debugging tools for memory leaks and corruption
- Overrides global `new`/`delete` operators
- Handles W3D (W3D model format) memory pools

## Key Types
- **MemoryPoolSingleBlock (Class)**: Represents individual memory blocks within a pool
- **MemoryPoolBlob (Class)**: Manages collections of memory blocks (containers for `MemoryPoolSingleBlock`)
- **STLSpecialAlloc (Class)**: Custom allocator for STL containers
- **BlockCheckpointInfo (Class)**: Debugging structure for tracking block allocation history (conditional)

## Key Functions
### `initMemoryManager`
- Purpose: Initializes the memory manager and creates global allocators
- Calls: `userMemoryManagerGetDmaParms`, `MemoryPoolFactory::init`, `createDynamicMemoryAllocator`, `userMemoryManagerInitPools`

### `preMainInitMemoryManager`
- Purpose: Early initialization for memory allocations before main()
- Calls: `userMemoryManagerGetDmaParms`, `MemoryPoolFactory::init`, `createDynamicMemoryAllocator`, `userMemoryManagerInitPools`

### `shutdownMemoryManager`
- Purpose: Cleans up memory manager resources
- Calls: `destroyDynamicMemoryAllocator`, `MemoryPoolFactory::~MemoryPoolFactory`, `sysFree`

### `operator new`/`operator delete`
- Purpose: Override global allocation operators
- Calls: `preMainInitMemoryManager`, `TheDynamicMemoryAllocator->allocateBytes/freeBytes`

### `createW3DMemPool`
- Purpose: Creates memory pools for W3D assets
- Calls: `TheMemoryPoolFactory->createMemoryPool`

## Globals
- **thePreMainInitFlag (Bool)**: Tracks if pre-main initialization occurred
- **theMainInitFlag (Bool)**: Tracks if main initialization occurred
- **TheMemoryPoolFactory (MemoryPoolFactory*)**: Global memory pool factory instance
- **TheDynamicMemoryAllocator (DynamicMemoryAllocator*)**: Global dynamic allocator instance
- **theLinkTester (int)**: Link verification counter

## Dependencies
- `GameMemory.h`, `CriticalSection.h`, `Errors.h`, `GlobalData.h`, `PerfTimer.h`
- Windows API (`GlobalAlloc`, `GlobalFree`)
- STL containers (conditional)
- Debug logging system
