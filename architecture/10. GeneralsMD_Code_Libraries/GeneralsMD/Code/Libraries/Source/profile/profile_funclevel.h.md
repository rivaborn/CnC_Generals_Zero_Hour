# GeneralsMD/Code/Libraries/Source/profile/profile_funclevel.h

## Purpose
Defines the `ProfileFuncLevel` class for function-level profiling in the game engine.

## Responsibilities
- Provides profiling data for functions (calls, time, callers)
- Manages thread-specific profiling information
- Enumerates profiled threads and their functions
- Exposes profiling metrics via `Id` and `Thread` classes

## Key Types
- **ProfileFuncLevel (Class)**: Main profiler class (singleton)
- **Id (Class)**: Represents a profiled function with metrics access
- **Thread (Class)**: Represents a profiled thread
- **IdList (Class)**: List of function IDs
- **(anonymous enum) (Enum)**: Special frame numbers (e.g., `Total`)

## Key Functions
### `Id::GetCalls`
- Purpose: Returns call count for a function in a given frame.
- Calls: Not inferable (internal implementation).

### `Id::GetTime`
- Purpose: Returns total time spent in a function (including children) for a frame.
- Calls: Not inferable.

### `Id::GetFunctionTime`
- Purpose: Returns time spent only in the function (excluding children) for a frame.
- Calls: Not inferable.

### `Thread::EnumProfile`
- Purpose: Enumerates profiled functions for a thread.
- Calls: Not inferable.

### `ProfileFuncLevel::EnumThreads`
- Purpose: Enumerates all profiled threads.
- Calls: Not inferable.

## Globals
- **ProfileFuncLevel::Instance (ProfileFuncLevel)**: Singleton instance of the profiler.

## Dependencies
- Key includes: None visible in header.
- External symbols: `Profile` (friend class), `ProfileFuncLevelTracer` (internal type).
