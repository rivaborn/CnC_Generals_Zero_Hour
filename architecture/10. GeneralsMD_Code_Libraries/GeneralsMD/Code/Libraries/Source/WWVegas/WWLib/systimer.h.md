# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/systimer.h

## Purpose
Provides a wrapper class for Windows' timeGetTime() to track elapsed time in milliseconds.

## Responsibilities
- Wraps system time retrieval with overflow handling
- Tracks time since initialization
- Provides global time access via SystemTime instance

## Key Types
- SysTimeClass (Class): manages system time with overflow protection

## Key Functions
### SysTimeClass::Get
- Purpose: Returns elapsed time in milliseconds since initialization
- Calls: timeGetTime()

### SysTimeClass::Reset
- Purpose: Resets the timer and calculates wrap-around compensation
- Calls: timeGetTime()

### SysTimeClass::Is_Getting_Late
- Purpose: Checks if timer is approaching overflow
- Calls: None

## Globals
- SystemTime (SysTimeClass): Global timer instance

## Dependencies
- <windows.h> for timeGetTime()
- <mmsys.h> for multimedia timer functions
- "always.h" for WWINLINE macro
