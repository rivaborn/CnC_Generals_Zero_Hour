# Generals/Code/Libraries/Source/WWVegas/WWLib/systimer.h

## Purpose
Provides a wrapper class for Windows' timeGetTime() to track elapsed time with wrap-around handling.

## Responsibilities
- Wraps system time retrieval via timeGetTime()
- Handles timer wrap-around (overflow) scenarios
- Provides global time access via SystemTime instance
- Offers reset and late-check functionality

## Key Types
- **SysTimeClass (Class)**: Wrapper for system time tracking with wrap-around handling.

## Key Functions
### SysTimeClass::Get
- Purpose: Retrieves current elapsed time in milliseconds.
- Calls: timeGetTime(), Reset()

### SysTimeClass::Reset
- Purpose: Resets the timer to current time and calculates wrap-around value.
- Calls: timeGetTime()

### SysTimeClass::Is_Getting_Late
- Purpose: Checks if timer is approaching wrap-around.
- Calls: None

## Globals
- **SystemTime (SysTimeClass)**: Global instance for system time access.

## Dependencies
- `<windows.h>` for Windows API
- `<mmsys.h>` for timeGetTime()
- `always.h` (custom header)
- WWINLINE macro (custom inline specifier)
