# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.h - Enhanced Analysis

## Architectural Role
Central debug utility header providing cross-cutting diagnostic capabilities for the SAGE engine. Acts as the primary interface for debug logging, assertions, profiling, and system error handling across all subsystems.

## Cross-References
### Incoming
- Debug-related macros used throughout engine (game logic, rendering, networking)
- Assertions in core systems (memory, file I/O, W3D rendering)
- Profiling hooks in performance-critical code paths

### Outgoing
- Calls into Windows system error APIs
- Integrates with `debug.h` for build-conditional debug features
- Uses C runtime `printf` formatting

## Design Patterns
- **Strategy Pattern**: Installable handler functions for messages, assertions, triggers, and profiling allow runtime behavior customization
- **Preprocessor Directives**: Heavy use of conditional compilation to separate debug/release functionality
- **Facade Pattern**: Provides simplified macro interface (e.g., `WWASSERT`) hiding underlying complexity

*Not inferable*: Exact implementation of handler installation mechanisms or thread-safety guarantees.
