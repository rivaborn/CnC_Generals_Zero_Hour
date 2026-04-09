# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwmemlog.cpp

## Purpose
Implements memory allocation tracking and categorization for the SAGE engine, with thread-safe logging and category-based memory statistics.

## Responsibilities
- Tracks memory allocations and deallocations by category
- Manages thread-specific active memory categories
- Provides peak/current memory usage statistics
- Handles mutex locking for thread safety
- Integrates with custom new/delete operators

## Key Types
- **MemoryCounterClass (Class)**: Tracks current/peak memory usage per category
- **ActiveCategoryStackClass (Class)**: Manages category stack per thread
- **ActiveCategoryClass (Class)**: Handles multiple thread stacks
- **MemLogClass (Class)**: Central logging class
- **MemLogMutexLockClass (Class)**: RAII mutex wrapper
- **MemoryLogStruct (Struct)**: Header prepended to allocations

## Key Functions
### Allocate_Memory
- Purpose: Allocates memory with tracking header
- Calls: Register_Memory_Allocated, malloc

### Release_Memory
- Purpose: Frees memory and updates tracking
- Calls: Register_Memory_Released, free

### Get_Log
- Purpose: Lazy-initializes and returns MemLogClass instance
- Calls: W3DNEW, atexit

## Globals
- **AllocateCount (unsigned)**: Counts allocations since reset
- **FreeCount (unsigned)**: Counts frees since reset
- **_MemoryCategoryNames (char**)**: Category name lookup table
- **_TheMemLog (MemLogClass**)**: Singleton log instance
- **_MemLogMutex (void**)**: Mutex handle
- **_MemLogAllocated (bool)**: Tracks if log was allocated

## Dependencies
- wwmemlog.h, wwdebug.h, vector.h, windows.h
- W3DNEW, WWASSERT macros
- ::GetCurrentThreadId, ::malloc, ::free, atexit
