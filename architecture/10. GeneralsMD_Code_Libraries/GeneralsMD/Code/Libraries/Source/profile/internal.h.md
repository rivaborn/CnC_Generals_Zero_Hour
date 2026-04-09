# GeneralsMD/Code/Libraries/Source/profile/internal.h

## Purpose
Internal header for profiling utilities, including thread-safe critical sections and timing functions.

## Responsibilities
- Defines `ProfileFastCS` for thread-safe synchronization
- Provides memory allocation/deallocation hooks for profiling
- Implements high-resolution timing via `ProfileGetTime`
- Declares internal profiling command interfaces

## Key Types
- **ProfileFastCS (Class)**: Thread-safe critical section using atomic bit operations
- **ProfileFastCS::Lock (Class)**: RAII lock wrapper for `ProfileFastCS`
- **HANDLE (Type)**: Windows handle for synchronization event

## Key Functions
### `ProfileAllocMemory`
- Purpose: Allocate memory with profiling instrumentation
- Calls: Not inferable

### `ProfileReAllocMemory`
- Purpose: Reallocate memory with profiling instrumentation
- Calls: Not inferable

### `ProfileFreeMemory`
- Purpose: Free memory with profiling instrumentation
- Calls: Not inferable

### `ProfileGetTime`
- Purpose: Read high-resolution CPU timestamp into 64-bit integer
- Calls: Uses `rdtsc` CPU instruction

## Globals
- **ProfileFastCS::testEvent (HANDLE)**: Synchronization event for fallback locking

## Dependencies
- `"../debug/debug.h"` (for `DASSERT`)
- `"internal_funclevel.h"`
- `"internal_highlevel.h"`
- `"internal_cmd.h"`
- `"internal_result.h"`
- Windows API (`HANDLE`, `WaitForSingleObject`)
