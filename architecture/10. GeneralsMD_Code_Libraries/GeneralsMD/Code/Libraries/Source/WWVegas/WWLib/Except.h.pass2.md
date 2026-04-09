# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Except.h - Enhanced Analysis

## Architectural Role
This header defines the SAGE engine's exception handling and thread management infrastructure, critical for crash recovery and debugging in a real-time game. It bridges Windows-specific exception handling with the engine's modular architecture, enabling robust error recovery and thread tracking.

## Cross-References
### Incoming
- Likely called by core engine modules (e.g., `GameLoop`, `ThreadManager`) for exception registration and thread tracking.
- Used by debugging tools or post-mortem dump generators (e.g., `CrashHandler`).

### Outgoing
- Relies on Windows API (`win.h`) for exception handling primitives.
- Interfaces with thread management subsystems (e.g., `ThreadManager`) for thread registration.

## Design Patterns
- **Callback Pattern**: `Register_Application_Exception_Callback` allows modular exception handling.
- **Registry Pattern**: Thread registration/unregistration tracks active threads for debugging.
- **State Capsule**: Global variables (`ExceptionReturn*`) encapsulate recovery state for crash resilience.

*Not inferable*: No clear use of Factory, Observer, or Visitor patterns.
