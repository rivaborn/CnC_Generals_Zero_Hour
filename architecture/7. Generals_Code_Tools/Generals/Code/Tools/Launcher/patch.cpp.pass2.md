# Generals/Code/Tools/Launcher/patch.cpp - Enhanced Analysis

## Architectural Role
This file implements the patching subsystem for the game launcher, bridging between the patch discovery logic (findpatch.cpp) and the actual patching engine (patchw32.dll). It handles UI feedback, registry updates, and system-level operations required for game updates.

## Cross-References
### Incoming
- `findpatch.cpp` calls `Apply_Patch` to execute discovered patches
- `findpatch.cpp` references `PatchCallBack` for progress reporting

### Outgoing
- Calls into `patchw32.dll` (RTPatchApply32) for actual patching
- Uses Windows API for registry operations, process management, and UI
- References `launcher.txt` for patch information display

## Design Patterns
- **Callback Pattern**: `PatchCallBack` implements a callback interface for progress reporting during patching
- **Command Pattern**: `Apply_Patch` encapsulates the patching operation as a self-contained command
- **Registry Pattern**: Uses Windows registry for persistent patch state tracking

Not inferable: No clear use of Factory, Observer, or Strategy patterns in the visible code.
