# GeneralsMD/Code/Libraries/Source/profile/profile_highlevel.cpp - Enhanced Analysis

## Architectural Role
This file implements the high-level profiling infrastructure used across the SAGE engine for performance monitoring. It provides thread-safe, frame-aware profiling capabilities that are likely used by game systems, rendering, AI, and other subsystems to track execution metrics.

## Cross-References
### Incoming
- Game systems (rendering, AI, etc.) use `ProfileHighLevel::Block` for scoped timing
- Other profiling components call `AddProfile` to register metrics
- Frame management systems call `FrameStart`/`FrameEnd` for frame-based recording

### Outgoing
- Calls into low-level profiling utilities (`ProfileGetTime`, memory allocators)
- Uses `ProfileFastCS` for thread synchronization
- Interacts with `ProfileId` for core profiling data management

## Design Patterns
- **Singleton**: `ProfileHighLevel::Instance` provides global access to profiling
- **RAII**: `Block` class manages timing scope automatically
- **Flyweight**: String formatting uses a shared buffer to reduce allocations

*Not inferable*: Exact usage patterns by other subsystems without cross-referencing callers.
