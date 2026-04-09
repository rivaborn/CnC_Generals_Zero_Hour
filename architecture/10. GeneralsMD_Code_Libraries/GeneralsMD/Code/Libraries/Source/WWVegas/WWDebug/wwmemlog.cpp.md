# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwmemlog.cpp

## Purpose
Implements a memory logging system for tracking allocations and deallocations by category in a thread-safe manner.

## Responsibilities
- Tracks memory allocations and releases per category
- Manages thread-specific active memory categories
- Provides peak/current memory usage statistics
- Handles synchronization via mutexes/critical sections

## Key Types
- **MemoryCounterClass (Class)**: Tracks current/peak memory usage per category
- **ActiveCategoryStackClass (Class)**: Manages per-thread memory category stack
- **ActiveCategoryClass (Class)**: Handles multiple thread stacks for active categories
- **MemLogClass (Class)**: Core logging class tying all components together
- **MemLogMutexLockClass (Class)**: RAII wrapper for mutex locking
- **MemoryLogStruct (Struct)**: Header prepended to allocations for tracking

## Key Functions
### Allocate_Memory
- Purpose: Allocates memory with a tracking header
- Calls: Register_Memory_Allocated, MemoryLogStruct constructor

### Release_Memory
- Purpose: Frees memory and updates tracking
- Calls: Register_Memory_Released

### Get_Log
- Purpose: Lazy-initializes and returns the global MemLog instance
- Calls: None (but creates MemLogClass instance)

## Globals
- **AllocateCount (unsigned)**: Counts total allocations
- **FreeCount (unsigned)**: Counts total deallocations
- **_MemoryCategoryNames (char**)**: Array of category name strings
- **_TheMemLog (MemLogClass**)**: Global logging instance
- **WWMEMLOG_KEY0/1 (int)**: Magic values for header validation

## Dependencies
- Key includes: "wwmemlog.h", "wwdebug.h", "vector.h", "fastallocator.h", <windows.h>
- External symbols: FastAllocatorGeneral, ThreadClass, W3DNEW, atexit, GetCurrentThreadId, CreateMutex, WaitForSingleObject, ReleaseMutex, InitializeCriticalSection, EnterCriticalSection, LeaveCriticalSection
