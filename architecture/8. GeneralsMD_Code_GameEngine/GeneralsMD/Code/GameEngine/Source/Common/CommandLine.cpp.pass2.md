# GeneralsMD/Code/GameEngine/Source/Common/CommandLine.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central command-line parsing hub, bridging user input with the engine's configuration system. It directly modifies `TheWritableGlobalData` and other engine globals, making it a critical early-boot component that influences nearly all subsystems.

## Cross-References
### Incoming
- **Game Entry Point**: Likely called from `main()` or equivalent in the executable
- **Mod System**: `TheArchiveFileSystem->loadMods()` called at end of parsing
- **Debug Systems**: `DEBUG_LOG` and `DEBUG_CRASH` macros used throughout

### Outgoing
- **Global Data**: Modifies `TheWritableGlobalData` (windowed mode, audio, etc.)
- **File Systems**: Uses `TheLocalFileSystem` and `TheArchiveFileSystem`
- **Debug Systems**: Calls `DebugSetFlags` and `DEBUG_LOG`
- **Version System**: References `TheVersion`

## Design Patterns
- **Command Pattern**: Each flag handler is a command object (function pointer) in the `params` array
- **Table-Driven Parsing**: Uses a lookup table (`CommandLineParam[]`) for dispatch
- **Early Initialization**: Modifies globals before most systems are initialized

*Not inferable*: No clear use of other patterns like Factory or Observer in this file.
