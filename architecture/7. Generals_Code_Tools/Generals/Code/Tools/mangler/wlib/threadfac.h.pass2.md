# Generals/Code/Tools/mangler/wlib/threadfac.h - Enhanced Analysis

## Architectural Role
This header defines the core threading abstraction layer for the SAGE engine, enabling cross-platform thread creation and management. It bridges platform-specific APIs (Win32/POSIX) with higher-level game systems needing concurrent execution.

## Cross-References
### Incoming
- `matchbot/wlib/threadfac.h` (duplicate file in another tool directory)
- Likely called by game logic threads (e.g., AI, networking) and toolchain utilities

### Outgoing
- Uses `CritSec` (from `critsec.h`) for thread-safe counter management
- Platform-specific headers (`pthread.h`/`process.h`)

## Design Patterns
- **Factory Pattern**: `ThreadFactory` centralizes thread creation logic
- **Template Method**: `Runnable::run()` as virtual entry point for derived classes
- **Singleton-like**: Static methods with internal state (`ThreadCount_`)

*Not inferable*: Exact usage patterns in game code (e.g., which subsystems spawn threads).
