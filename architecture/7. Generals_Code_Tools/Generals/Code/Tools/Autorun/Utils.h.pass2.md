# Generals/Code/Tools/Autorun/Utils.h - Enhanced Analysis

## Architectural Role
This header provides low-level utility functions used across the Autorun toolchain, serving as a shared dependency for string manipulation, file I/O, and path handling. Its functions are likely called by build scripts, asset processors, and other tooling components.

## Cross-References
### Incoming
- `Generals/Code/Tools/Autorun/*.cpp` (Autorun toolchain)
- `Generals/Code/Tools/AssetBuilders/*.cpp` (Asset processing tools)
- `Generals/Code/Tools/ScriptCompilers/*.cpp` (Script compilation tools)

### Outgoing
- Windows API (`<windows.h>`) for file operations and string handling
- Standard C runtime for memory allocation and file I/O

## Design Patterns
- **Utility Class Pattern**: Functions are stateless and operate on passed parameters, typical for utility libraries.
- **Template Method**: `swap<T>` demonstrates generic programming for type-agnostic swapping.
- **Not inferable**: No other patterns are clearly evident from the header alone.
