# GeneralsMD/Code/Libraries/Source/profile/profile_highlevel.h - Enhanced Analysis

## Architectural Role
This header defines the high-level profiling interface used across the engine for performance monitoring. It provides a singleton-based profiling system that tracks metrics like frame times, resource counts, and other runtime statistics, critical for both development diagnostics and in-game performance displays.

## Cross-References
### Incoming
- Likely called by rendering subsystems (e.g., texture loading, draw calls)
- Used by game logic systems (e.g., AI decision timing, unit processing)
- Accessed by UI systems for displaying performance metrics

### Outgoing
- Depends on `ProfileId` (internal implementation)
- Uses `_int64` for timing (Windows SDK)
- Interfaces with lower-level profiling mechanisms (not exposed in header)

## Design Patterns
- **Singleton**: Ensures single instance of `ProfileHighLevel` for global profiling state
- **RAII**: `Block` class uses constructor/destructor for automatic timing scope management
- **Flyweight**: `Id` class acts as a lightweight handle to shared profiling data

*Not inferable*: Exact relationship with lower-level profiling backend or thread-safety mechanisms.
