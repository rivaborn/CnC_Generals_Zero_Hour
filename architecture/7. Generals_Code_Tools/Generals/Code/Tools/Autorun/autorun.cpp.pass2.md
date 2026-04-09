# Generals/Code/Tools/Autorun/autorun.cpp - Enhanced Analysis

## Architectural Role
This file implements the autorun functionality for the game's installation media, serving as the entry point for CD-based launches. It bridges the gap between physical media verification and game execution, handling UI presentation, localization, and process launching.

## Cross-References
### Incoming
- `Generals/Code/Tools/Autorun/resource.h` (resource definitions)
- `Generals/Code/Tools/Autorun/drawbutton.h` (UI button rendering)
- `Generals/Code/Tools/Autorun/args.h` (command-line argument parsing)
- `Generals/Code/Tools/Autorun/cdcntrl.h` (CD drive detection)

### Outgoing
- Windows API (process creation, message handling)
- `WSYS_FileSystem.h` (file system abstraction)
- `GameText.h` (localization)
- `Locale_API.h` (language support)

## Design Patterns
- **Command Pattern**: `LaunchObjectClass` encapsulates process launching logic
- **Singleton**: Global `MainWindow` instance manages the autorun UI
- **Adapter Pattern**: `LaunchObjectClass` adapts Windows process creation to game-specific needs

*Not inferable*: Exact implementation of CD verification or sound management patterns.
