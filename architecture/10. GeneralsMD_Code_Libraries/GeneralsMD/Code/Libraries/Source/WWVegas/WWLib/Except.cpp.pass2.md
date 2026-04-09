# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Except.cpp - Enhanced Analysis

## Architectural Role
This file is the central exception handling subsystem for the SAGE engine, providing crash reporting and debugging infrastructure. It bridges low-level Windows exception handling with game-specific error recovery mechanisms.

## Cross-References
### Incoming
- Game logic modules (e.g., mission loading, AI) likely register callbacks via `Register_Application_Exception_Callback`
- Thread management system registers threads in `ThreadList`
- Debugging tools may query `SymbolsAvailable` or call `Stack_Walk`

### Outgoing
- Dynamically loads `IMAGEHLP.DLL` for symbol resolution
- Interacts with Windows API for exception handling (`SetUnhandledExceptionFilter`)
- Uses `WWDebug` subsystem for logging (`DebugString`)

## Design Patterns
- **Callback Pattern**: Uses `AppCallback` and `AppVersionCallback` to delegate exception handling to game-specific logic
- **Lazy Initialization**: Loads `IMAGEHLP.DLL` functions only when needed (`Load_Image_Helper`)
- **Resource Management**: Explicit cleanup of symbol handler resources via `_SymCleanup`

*Not inferable*: No clear use of Singleton or Factory patterns in the provided snippet.
