# Generals/Code/Libraries/Source/WWVegas/WWLib/argv.h - Enhanced Analysis

## Architectural Role
This file provides a lightweight, reusable command-line argument parser used during game initialization. It bridges the OS-specific entry point (WinMain) with the game's configuration system, allowing both direct command-line flags and external config files to influence runtime behavior.

## Cross-References
### Incoming
- Likely called from `main.cpp`/`WinMain` entry point
- Possibly referenced by debug/build systems (e.g., for `-debug`, `-log` flags)
- May be used by modding tools to inject custom arguments

### Outgoing
- Uses `always.h` for basic macros/types
- Conditionally includes `osdep.h` for platform-specific handling
- No direct subsystem calls; operates at a low level

## Design Patterns
- **Singleton-like static state**: `Argc`/`Argv` are static, implying shared state across the program
- **Iterator pattern**: `First()`/`Next()`/`Cur()` for argument traversal
- **Strategy pattern**: Case sensitivity/exact size matching as runtime-configurable flags

*Not inferable*: No clear use of Factory, Observer, or other patterns.
