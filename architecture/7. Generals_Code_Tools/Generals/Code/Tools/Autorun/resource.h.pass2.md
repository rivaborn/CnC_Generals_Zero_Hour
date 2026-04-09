# Generals/Code/Tools/Autorun/resource.h - Enhanced Analysis

## Architectural Role
This file is part of the Autorun tool, which is a Windows installer helper. It defines resource IDs for dialog boxes and strings used in the installer UI, bridging the game's installation process with Windows shell integration.

## Cross-References
### Incoming
- `Generals/Code/Tools/Autorun/AUTORUN.RC` (Microsoft Resource Compiler input file)

### Outgoing
- None (resource definitions are passive, referenced by RC file and linker)

## Design Patterns
- **Resource Pattern**: Uses Windows resource definitions for UI elements, following Microsoft's resource compilation model.
- **Constant Pool**: Groups related constants (dialog IDs, string IDs) for maintainability.
