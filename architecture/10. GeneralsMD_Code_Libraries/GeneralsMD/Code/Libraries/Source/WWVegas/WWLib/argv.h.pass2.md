# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/argv.h - Enhanced Analysis

## Architectural Role
This file provides the core command-line argument parsing infrastructure for the SAGE engine, enabling both direct command-line arguments and file-based configuration loading. It serves as a foundational utility for game initialization and configuration management.

## Cross-References
### Incoming
- Likely called by `main.cpp`/`WinMain` for initial argument parsing
- Potentially used by debug/build systems for runtime configuration
- May be referenced by modding tools for parameter file generation

### Outgoing
- Uses `always.h` for basic macros and types
- Conditionally includes `osdep.h` for platform-specific handling
- No direct subsystem calls inferred (pure utility class)

## Design Patterns
- **Singleton-like static management**: Global `Argc`/`Argv` state with static methods
- **Iterator pattern**: `Find()`/`Next()`/`Cur()` for argument traversal
- **Strategy pattern**: Configurable case sensitivity/exact size matching via flags

*Not inferable*: No clear use of factory, observer, or other complex patterns.
