# Generals/Code/Tools/Launcher/process.h

## Purpose
Defines a `Process` class and related functions for process management on Windows.

## Responsibilities
- Encapsulates process creation and monitoring
- Provides process info storage (handles, IDs, paths)
- Exposes functions to read, create, and wait on processes

## Key Types
- Process (Class): Wraps Windows process/thread handles and identifiers

## Key Functions
### Read_Process_Info
- Purpose: Reads process configuration from a ConfigFile.
- Calls: Not inferable (implementation in .cpp)

### Create_Process
- Purpose: Creates a process based on Process object fields.
- Calls: Not inferable

### Wait_Process
- Purpose: Waits for process termination and optionally retrieves exit code.
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<windows.h>`: Win32 API headers
- `"wstypes.h"`: Custom types (bit8)
- `"wdebug.h"`: Debug utilities
- `"configfile.h"`: Configuration file handling
