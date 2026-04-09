# GeneralsMD/Code/GameEngine/Source/Common/System/StackDump.cpp - Enhanced Analysis

## Architectural Role
This file is part of the engine's debugging infrastructure, providing low-level stack tracing and exception handling capabilities. It bridges the Windows API (via DbgHelp) with the game's internal logging system, enabling crash diagnostics in debug builds.

## Cross-References
### Incoming
- **Exception Handler**: Likely called by the game's global exception handler (not shown in file)
- **Debug Builds**: Invoked by internal debug utilities or crash reporters

### Outgoing
- **Windows API**: Uses `DbgHelp.lib` for symbol resolution (`SymInitialize`, `StackWalk`, etc.)
- **Internal Debugging**: Outputs to `DEBUG_LOG` and `g_LastErrorDump` (shared global)

## Design Patterns
- **Callback Pattern**: Uses function pointers (`void (*callback)(const char*)`) for flexible output routing (e.g., logging or UI display)
- **Lazy Initialization**: Symbol info is initialized only when needed (`InitSymbolInfo`/`UninitSymbolInfo`)
- **Adapter Pattern**: Wraps Windows-specific APIs (`CONTEXT`, `STACKFRAME`) into game-agnostic stack trace utilities

*Not inferable*: No clear use of Singleton or Factory patterns; dependencies are direct.
