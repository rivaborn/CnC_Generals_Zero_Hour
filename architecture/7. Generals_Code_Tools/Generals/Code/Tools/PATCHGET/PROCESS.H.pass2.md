# Generals/Code/Tools/PATCHGET/PROCESS.H - Enhanced Analysis

## Architectural Role
This file is part of the PATCHGET tool's process management subsystem, providing low-level Windows process creation and synchronization. It abstracts process handling for patching operations, likely used during game installation or update workflows.

## Cross-References
### Incoming
- Not inferable (no callers visible in this file)

### Outgoing
- Calls Windows API (`CreateProcess`, `WaitForSingleObject`) via `HANDLE`/`DWORD` usage
- Likely calls into `wstypes.h` for `bit8` (custom boolean type)

## Design Patterns
- **Facade Pattern**: Wraps Windows process APIs behind simpler `Create_Process`/`Wait_Process` functions
- **Data Transfer Object**: `Process` class acts as a DTO for process configuration
- **Not inferable**: No clear use of other patterns (e.g., no inheritance, polymorphism visible)
