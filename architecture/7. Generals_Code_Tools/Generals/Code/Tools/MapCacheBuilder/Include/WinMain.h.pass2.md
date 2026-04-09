# Generals/Code/Tools/MapCacheBuilder/Include/WinMain.h - Enhanced Analysis

## Architectural Role
This header provides the Windows application entry point infrastructure for the MapCacheBuilder tool, a utility in the SAGE engine's toolchain. It bridges the tool with the Windows API, enabling standalone execution separate from the main game process.

## Cross-References
### Incoming
- Likely referenced by `MapCacheBuilder.cpp` (main tool implementation)
- Potentially used by other tool-specific modules needing the global instance handle

### Outgoing
- Directly depends on `<windows.h>` for Windows API definitions
- No other subsystem dependencies inferred (tool-specific isolation)

## Design Patterns
- **Global Instance Pattern**: Exposes `ApplicationHInstance` as a global handle, common in Windows applications for resource management
- **Header Guard Pattern**: Uses `#pragma once` and traditional `#ifndef` guards to prevent multiple inclusions
- **Minimalist Design**: Focuses solely on Windows application infrastructure, avoiding game engine dependencies

*Not inferable*: No other patterns evident from this header alone.
