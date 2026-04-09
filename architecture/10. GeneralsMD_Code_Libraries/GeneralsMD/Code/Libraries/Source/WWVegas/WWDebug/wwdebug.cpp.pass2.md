# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.cpp - Enhanced Analysis

## Architectural Role
This file is the central debug utility module for the SAGE engine, providing a pluggable architecture for debug output, assertions, triggers, and profiling. It serves as the foundation for all debug-related functionality across the engine.

## Cross-References
### Incoming
- Game logic modules (e.g., AI, rendering) call `WWDebug_Printf` family for logging
- Assertion macros throughout the codebase invoke `WWDebug_Assert_Fail`
- Profiling systems use `WWDebug_Profile_Start/Stop`
- Debug triggers are checked via `WWDebug_Check_Trigger`

### Outgoing
- Uses Windows API (`FormatMessage`, `GetLastError`) for system error handling
- Relies on C runtime for string formatting (`vsprintf`)
- Interfaces with `except.h` for exception handling integration

## Design Patterns
- **Strategy Pattern**: Debug handlers are interchangeable strategies (message/assert/trigger/profile)
- **Callback Pattern**: Core functionality is delegated to user-provided callbacks
- **Facade Pattern**: Simplifies complex debug operations behind a clean interface

*Not inferable*: No clear use of Observer or Singleton patterns in this file.
