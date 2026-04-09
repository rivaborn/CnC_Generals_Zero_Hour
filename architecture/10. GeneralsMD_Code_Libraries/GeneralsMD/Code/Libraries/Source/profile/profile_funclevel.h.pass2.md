# GeneralsMD/Code/Libraries/Source/profile/profile_funclevel.h - Enhanced Analysis

## Architectural Role
This header defines the core interface for the SAGE engine's function-level profiling system, enabling performance analysis of game code. It abstracts low-level profiling data into thread and function-centric objects, supporting both real-time and post-mortem analysis.

## Cross-References
### Incoming
- **Profile** (friend class): Likely the main profiling controller that instantiates and manages `ProfileFuncLevel`
- **Game logic modules**: Any subsystem using `PROFILE_BEGIN/END` macros (not shown here) would indirectly depend on this interface

### Outgoing
- **ProfileFuncLevelTracer** (internal): Handles actual thread-specific profiling data collection
- **Low-level timing APIs**: Uses CPU tick counters (via `GetTime`/`GetFunctionTime`)

## Design Patterns
- **Singleton**: `ProfileFuncLevel::Instance` ensures single profiler instance
- **Facade**: Hides complex profiling data behind simple `Id`/`Thread` interfaces
- **Iterator**: `IdList` and `Enum` methods provide traversal of profiling data

*Not inferable*: Exact relationship with `Profile` class or macro-based instrumentation system.
