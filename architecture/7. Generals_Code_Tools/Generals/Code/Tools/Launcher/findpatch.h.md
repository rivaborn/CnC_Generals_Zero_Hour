# Generals/Code/Tools/Launcher/findpatch.h

## Purpose
Header file declaring functions for locating and managing game patches.

## Responsibilities
- Declares patch search and deletion functions
- Provides app directory retrieval
- Defines interface for patch management

## Key Types
None

## Key Functions
### Find_Patch
- Purpose: Locates a patch file based on configuration
- Calls: Not inferable

### Get_App_Dir
- Purpose: Retrieves application directory path from config
- Calls: Not inferable

### Delete_Patches
- Purpose: Removes installed patches
- Calls: Not inferable

## Globals
None

## Dependencies
- `<stdlib.h>`, `<stdio.h>`, `<windows.h>`, `<direct.h>`
- `wstypes.h`, `configfile.h`
- `ConfigFile` class, `bit8` type, `OUT` macro
