# Generals/Code/Tools/Launcher/findpatch.cpp - Enhanced Analysis

## Architectural Role
This file is part of the launcher toolchain, responsible for patch management during game installation/updates. It bridges the launcher UI with the Windows registry and filesystem to locate and clean up patch files.

## Cross-References
### Incoming
- Launcher UI (calls `Find_Patch` to locate patches)
- Patch application logic (calls `Delete_Patches` post-update)

### Outgoing
- Windows API (`RegOpenKeyEx`, `FindFirstFile`)
- ConfigFile class (for SKU configuration)
- Wstring class (for string manipulation)

## Design Patterns
- **Registry Query Pattern**: Uses `RegOpenKeyEx`/`RegQueryValueEx` to fetch installation paths, common in Windows-based installers.
- **File Enumeration Pattern**: Uses `FindFirstFile`/`FindNextFile` for directory scanning, standard for filesystem operations.
- **Not inferable**: No clear OOP patterns (e.g., no inheritance or polymorphism visible).

**Note**: The commented-out `_unlink` calls suggest this was part of a larger patch system where file deletion was disabled for safety.
