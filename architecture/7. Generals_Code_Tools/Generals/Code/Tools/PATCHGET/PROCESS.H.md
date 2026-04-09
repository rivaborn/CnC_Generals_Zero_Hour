# Generals/Code/Tools/PATCHGET/PROCESS.H

## Purpose
Defines a `Process` class and related functions for process creation and management in the PATCHGET tool.

## Responsibilities
- Declares a `Process` class to hold process execution details.
- Provides functions to create and wait on processes.
- Manages process handles and execution state.

## Key Types
- **Process (class)**: Encapsulates process execution details (directory, command, args, handles).
- **Create_Process (function)**: Creates a new process.
- **Wait_Process (function)**: Waits for a process to complete.

## Key Functions
### Create_Process
- Purpose: Creates a new process based on the given `Process` object.
- Calls: Not inferable (implementation in another file).

### Wait_Process
- Purpose: Waits for the specified process to terminate and optionally retrieves its exit code.
- Calls: Not inferable (implementation in another file).

## Globals
- None

## Dependencies
- `<windows.h>`: For Windows API types (`HANDLE`, `DWORD`).
- `"wstypes.h"`: Likely for custom types like `bit8`.
- `ConfigFile` (forward reference): Used in commented-out function.
