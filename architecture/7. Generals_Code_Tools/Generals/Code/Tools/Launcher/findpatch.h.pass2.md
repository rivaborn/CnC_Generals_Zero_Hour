# Generals/Code/Tools/Launcher/findpatch.h - Enhanced Analysis

## Architectural Role
This header defines the patch management interface for the game launcher, bridging the build tools and runtime environment. It abstracts patch location, retrieval, and cleanup operations, critical for modding and version control.

## Cross-References
### Incoming
- `Generals/Code/Tools/Launcher/launcher.cpp` (primary consumer)
- `Generals/Code/Tools/Launcher/main.cpp` (likely entry point)
- Modding tools (inferred from `ConfigFile` usage)

### Outgoing
- `configfile.h` (for configuration parsing)
- Windows API (`<windows.h>`, `<direct.h>`) for filesystem operations
- `wstypes.h` for type definitions

## Design Patterns
- **Dependency Injection**: `ConfigFile` is passed as a parameter, decoupling patch logic from config storage.
- **Facade Pattern**: Hides filesystem complexity behind simple functions like `Find_Patch`.
- **Not inferable**: No clear use of creational or behavioral patterns in the header.

*(Token count: 198)*
