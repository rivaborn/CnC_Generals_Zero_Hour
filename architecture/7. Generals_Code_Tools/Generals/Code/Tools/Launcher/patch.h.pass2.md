# Generals/Code/Tools/Launcher/patch.h - Enhanced Analysis

## Architectural Role
This header defines the core patching interface for the launcher, bridging the patch discovery (findpatch.h) and configuration systems. It's part of the toolchain's update mechanism, ensuring game binaries/configs align with the installed SKU.

## Cross-References
### Incoming
- `Generals/Code/Tools/Launcher/launcher.cpp` (likely calls `Apply_Patch` during startup)
- `Generals/Code/Tools/Launcher/findpatch.cpp` (uses `Get_App_Dir` for patch paths)

### Outgoing
- Relies on `ConfigFile` class for persistent configuration
- Uses `process.h` for potential binary patching (not just config)

## Design Patterns
- **Facade Pattern**: `Apply_Patch` abstracts patching complexity (file I/O, config updates, SKU validation)
- **Dependency Injection**: `ConfigFile` and `skuIndex` passed as parameters, enabling testability
- **Resource Management**: Implicit via `resource.h` for dialogs (error handling for failed patches)

*Not inferable*: No clear use of Singleton or Observer patterns in this header.
