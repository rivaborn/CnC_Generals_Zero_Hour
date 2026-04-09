# GeneralsMD/Code/Libraries/Source/profile/internal_funclevel.h - Enhanced Analysis

## Architectural Role
This file defines the core profiling infrastructure for the SAGE engine, enabling function-level performance analysis. It tracks call hierarchies, timing metrics, and frame-based profiling data, critical for optimizing game performance.

## Cross-References
### Incoming
- **ProfileCmdInterface**: Uses `ProfileFuncLevelTracer` as a friend class, suggesting command-line integration for profiling control.
- **Game Logic/Rendering Subsystems**: Likely instrumented with `Enter`/`Leave` calls to track performance-critical paths.

### Outgoing
- **No external dependencies**: Operates independently, focusing on internal profiling data structures.

## Design Patterns
- **Singleton-like Management**: Uses static `head` pointer for tracer instances, implying centralized profiling control.
- **Hash Map for Efficiency**: `UnsignedMap` and `FunctionMap` use custom hash tables to manage function addresses and caller relationships.
- **Frame-Based Buffering**: `MAX_FRAME_RECORDS` and `frameRecordMask` enable multi-frame profiling without real-time overhead.

**Not inferable**: Specific usage patterns in game logic or rendering subsystems.
