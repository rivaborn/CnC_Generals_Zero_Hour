# GeneralsMD/Code/GameEngine/Include/Common/MiniLog.h

## Purpose
Header for a lightweight logging utility used during debug builds.

## Responsibilities
- Provides a simple logging class for debug builds
- Manages file I/O for log output
- Supports variadic logging messages

## Key Types
- LogClass (class): Debug logging utility that writes to a file

## Key Functions
### LogClass::log
- Purpose: Writes a formatted message to the log file
- Calls: va_list handling (not visible in header)

## Globals
None

## Dependencies
- "Lib/BaseType.h"
- "GameLogic/GameLogic.h"
- <cstdarg>
- FILE (from C stdlib)
