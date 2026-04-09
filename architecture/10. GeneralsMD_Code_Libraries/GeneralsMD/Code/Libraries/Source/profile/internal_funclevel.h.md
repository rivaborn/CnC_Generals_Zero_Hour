# GeneralsMD/Code/Libraries/Source/profile/internal_funclevel.h

## Purpose
Internal header for function-level profiling in the SAGE engine, managing call stacks, timing, and frame-based profiling data.

## Responsibilities
- Tracks function call hierarchy and timing metrics
- Manages frame-based profiling data storage
- Provides interfaces for entering/leaving functions and frame management
- Handles recursion depth and caller relationships

## Key Types
- **ProfileFuncLevelTracer (Class)**: Main profiler class managing function calls and timing
- **UnsignedMap (Class)**: Hash map for unsigned integer values with collision handling
- **Profile (Struct)**: Contains call count, timing data, and caller relationships
- **Function (Struct)**: Represents a profiled function with address, name, and timing data
- **StackEntry (Struct)**: Tracks active function calls with timing information

## Key Functions
### Enter
- Purpose: Records function entry with timing and stack state
- Calls: None visible

### Leave
- Purpose: Records function exit and calculates timing
- Calls: None visible

### FrameStart/FrameEnd
- Purpose: Manages frame-based profiling boundaries
- Calls: None visible

### FindFunction/EnumFunction
- Purpose: Retrieves function profiling data
- Calls: None visible

## Globals
- **head (ProfileFuncLevelTracer*)**: Linked list head for tracer instances
- **shuttingDown (bool)**: Shutdown state flag
- **curFrame (int)**: Current profiling frame index
- **frameRecordMask (unsigned)**: Bitmask for active frame records
- **recordCaller (bool)**: Flag for caller tracking

## Dependencies
- Uses `__int64` for timing measurements
- No external library dependencies visible
- Internal to profiling subsystem (no game-specific types)
