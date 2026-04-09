# GeneralsMD/Code/Libraries/Source/profile/profile_funclevel.cpp

## Purpose
Implements function-level profiling for performance analysis, tracking call counts, execution time, and call stacks.

## Responsibilities
- Manages thread-local profiling data via TLS
- Tracks function entry/exit with timing
- Maintains call graphs and time measurements
- Handles frame-based profiling for periodic snapshots
- Provides API for querying profiling data

## Key Types
- **ProfileFuncLevelTracer (Class)**: Manages per-thread profiling state and call stack
- **Function (Class)**: Represents a profiled function with timing stats
- **Profile (Struct)**: Contains call counts and timing for a specific frame
- **UnsignedMap (Class)**: Hash map for tracking caller relationships
- **ProfileMap (Class)**: Maps frame numbers to profile data
- **FunctionMap (Class)**: Hash map for tracking profiled functions

## Key Functions
### `_penter`
- Purpose: Hook function entry points to start profiling
- Calls: `TlsGetValue`, `ProfileFuncLevelTracer::Enter`, `ProfileAllocMemory`

### `_pleave`
- Purpose: Hook function exits to stop profiling and record timing
- Calls: `TlsGetValue`, `ProfileFuncLevelTracer::Leave`

### `ProfileFuncLevelTracer::Enter`
- Purpose: Records function entry with timing and stack state
- Calls: `ProfileGetTime`, `func.Find`, `ProfileAllocMemory`

### `ProfileFuncLevelTracer::Leave`
- Purpose: Records function exit, calculates timing, and updates stats
- Calls: `ProfileGetTime`, `DCRASH`

### `ProfileFuncLevelTracer::FrameStart`
- Purpose: Begins a new profiling frame/snapshot
- Calls: `ProfileFastCS::Lock`, `func.Enumerate`

## Globals
- **TLSIndex (int)**: TLS slot index for thread-local storage
- **cs (ProfileFastCS)**: Critical section for thread safety
- **ProfileFuncLevel::Instance (ProfileFuncLevel)**: Singleton instance
- **ProfileFastCS::testEvent (HANDLE)**: Event object for synchronization

## Dependencies
- `_pch.h`, `../debug/debug.h`
- `ProfileFastCS`, `DebugStackwalk`, `ProfileAllocMemory`
- TLS API (`TlsAlloc`, `TlsGetValue`, `TlsSetValue`)
- Windows API (`CreateEvent`)
